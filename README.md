```py
from sanic import Sanic, response

app = Sanic(__name__)


@app.route("/<github_path>")
async def redirect(request, github_path):
    return response.redirect(f"https://github.com/soosBot-com/{github_path}")


if __name__ == "__main__":
    app.run(host="0.0.0.0", port=80)
```
