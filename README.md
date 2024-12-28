Here's a `README.md` file for your project: 

```markdown
# Youtube Search

An asynchronous Python library to search for YouTube videos and retrieve detailed metadata, such as video title, channel, views, and more.

## Features
- Search for YouTube videos using keywords.
- Retrieve video metadata such as ID, title, description, channel, duration, views, and more.
- Supports setting a maximum number of search results.
- Provides data in `dict` or `JSON` format.

## Installation
Ensure you have Python 3.7 or higher installed.
```

1. Clone the repository:
   ```bash
   git clone https://github.com/rafkix/youtube-search.git
   cd youtube-search
   ```

2. Install dependencies:
   ```bash
   pip install aiohttp
   ```

## Usage

```python
import asyncio
from async_youtube_search import AsyncYoutubeSearch

async def main():
    # Create an instance of YoutubeSearch
    search = YoutubeSearch("rafkix", max_results=5)

    # Fetch video results
    await search.fetch_results()

    # Get results as a dictionary
    videos = search.to_dict()
    print(videos)

    # Get results as JSON
    videos_json = search.to_json()
    print(videos_json)

# Run the script
asyncio.run(main())
```

## Methods

### `fetch_results()`
Fetches video search results asynchronously.

### `to_dict(clear_cache=True)`
Returns the search results as a Python dictionary.

- `clear_cache`: Clears the internal cache of video results if set to `True`.

### `to_json(clear_cache=True)`
Returns the search results as a JSON string.

- `clear_cache`: Clears the internal cache of video results if set to `True`.

## Example Output
```json
{
  "videos": [
    {
      "id": "abcd1234",
      "thumbnails": ["https://example.com/thumbnail.jpg"],
      "title": "Learn Python Programming",
      "long_desc": "An introductory tutorial to Python programming.",
      "channel": "Programming with John",
      "duration": "12:34",
      "views": "1.2M views",
      "publish_time": "3 weeks ago",
      "url_suffix": "/watch?v=abcd1234"
    }
  ]
}
```

## Requirements
- Python 3.7+
- aiohttp

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Author
**rafkix**

- GitHub: [rafkix](https://github.com/rafkix)
- YouTube: [rafkix](https://youtube.com/@rafkix)

---

Feel free to contribute, open issues, or suggest improvements!
```
