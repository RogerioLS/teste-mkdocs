# Full example

!!! example "Install"

    === "pip install (recommended)"
        ```python
        from sanic import Sanic
        from sanic.response import json
        from sanic_camelcase_middleware import Camelize

        app = Sanic(__name__)

        Camelize(app)


        @app.route("/post", methods=["POST"])
        async def test(request):
            return json({"is_camelcase": True, "message": request.json})


        if __name__ == "__main__":
            app.run(host="0.0.0.0", port=8000)
        ```

    === "git clone (for development)"
        ```bash
        git clone https://github.com/ultralytics/ultralytics
        cd ultralytics
        pip install -e .
        ```