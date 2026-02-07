![PyPI version](https://img.shields.io/pypi/v/python-notion-plus)
![Python](https://img.shields.io/badge/python->=3.12-blue)
![Development Status](https://img.shields.io/badge/status-stable-green)
![Maintenance](https://img.shields.io/maintenance/yes/2026)
![PyPI](https://img.shields.io/pypi/dm/python-notion-plus)
![License](https://img.shields.io/pypi/l/python-notion-plus)

---

# python-notion-plus
An enhanced Python client for the Notion API, providing a more user-friendly interface and additional features.

---

## Features
- Simplified API calls
- Automatic handling of pagination
- Support for Notion's database queries
- Easy-to-use methods for common tasks

---

## Requirements
- Python 3.9+
- Notion API token
- Notion database ID

---

## Installation
```bash
pip install python-notion-plus
```

---

## Configuration
The package uses environment variables for authentication and configuration:
```bash
# Required environment variables
NOTION_TOKEN=your_notion_api_token
```

---

## Examples
### Basic Usage
```python
import json

from python_notion_plus import NotionClient


notion_client = NotionClient(database_id='your_database_id')

notion_content = notion_client.get_database_content()
for page in notion_content:
    properties = notion_client.format_notion_page(page)
    formatted_data = json.dumps(properties, indent=4)

    print(f'notion_page_properties: {formatted_data}')
```

---

## 🤝 Contributing
If you have a helpful tool, pattern, or improvement to suggest:
Fork the repo <br>
Create a new branch <br>
Submit a pull request <br>
I welcome additions that promote clean, productive, and maintainable development. <br>

---

## 🙏 Thanks
Thanks for exploring this repository! <br>
Happy coding! <br>
