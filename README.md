# RSSHub

> 🍰 Everything can be RSS

RSSHub is a lightweight, easily extensible RSS generator that can create RSS feeds for any type of content.

This project is a Python implementation of the [original RSSHub](https://github.com/DIYgod/RSSHub).

**Actually writing crawlers in Python is more convenient than JS :p**

DEMO address: https://pyrsshub.vercel.app

## Community

Discord Server: [https://discord.gg/4BZBZuyx7p](https://discord.gg/4BZBZuyx7p)

## RSS Filtering

You can filter RSS content using the following query strings:

- include_title: Search titles (supports multiple keywords)
- include_description: Search descriptions
- exclude_title: Exclude titles
- exclude_description: Exclude descriptions
- limit: Limit number of items

## How to Contribute RSS

1. Fork this repository
2. Create a new spider directory and script in the spiders folder, write your crawler (refer to my [crawler tutorial](https://juejin.cn/post/6953881777756700709))
3. Add corresponding routes in main.py under blueprints (following existing route formats)
4. Write documentation in feeds.html under templates/main directory (follow existing formats)
5. Submit a PR

## Deployment

### Local Testing

First ensure [pipenv](https://github.com/pypa/pipenv) is installed

```bash
git clone https://github.com/alphardex/RSSHub-python
cd RSSHub-python
pipenv install --dev
pipenv shell
flask run
```

### Production Environment

```bash
gunicorn main:app -b 0.0.0.0:5000
```

### Deploy to Vercel

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2Fjp0id%2Frsshub-python)

### Docker Deployment

Create docker container: `docker run -dt --name pyrsshub -p 5000:5000 hillerliao/pyrsshub:latest`

## Requirements

- Python 3.8
