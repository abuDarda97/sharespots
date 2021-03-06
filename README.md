# Sharespots

Sharespots is a simple Django app that displays a curated list of cafes/co-working spaces to meetup and work in London.

<!--
@TODO Add auto table of contents after this issue is fixed
https://github.com/isaacs/github/issues/215
e.g. [TOC] or {:toc max_level=3 }
-->

## Technology Stack

- Backend: Python & Django
- Front-end: SASS/HTML5/JavaScript
- Hosting: Heroku
- Storage: AWS S3

## Software Tools Required

1. **Terminal**: [iTerm2](https://www.iterm2.com/) (MacOSX), [Terminator](http://gnometerminator.blogspot.co.uk/p/introduction.html) (Linux) or use your preferred one.
2. **Text Editor**: [Sublime Text](http://www.sublimetext.com/) or your preferred one.
3. [Docker Desktop](https://www.docker.com/products/docker-desktop)

## Project Setup

Open iTerm2 (or your preferred terminal.)

Clone the repo:

```shell
git clone git@github.com:PolyglotDevsLondon/sharespots.git
```

Change directory into the sharespots directory:

```shell
cd sharespots
```

[Download and install Docker Desktop](https://www.docker.com/products/docker-desktop) if you haven't already.

Build the docker container (included is django, postgres, pgadmin and jupyter notebook run from django_extensions):

```shell
docker-compose -f local.yml build
```

Fire up the docker container:

```shell
docker-compose -f local.yml up
```

Open project in your web browser at:

[http://0.0.0.0:8000/](http://0.0.0.0:8000/)

You should now see the Sharespots website (but no venue data will show yet.)

Open a new iTerm2 terminal tab by pressing ⌘T (or open an additional terminal window using your preferred terminal.)

Change to your sharespots directory:

```shell
cd [your/sharespot/directory]
```

Load seed data:

```shell
docker-compose -f local.yml run django python manage.py loaddata seed_data.json
```

Set up a super user for django admin:

```shell
docker-compose -f local.yml run django python manage.py createsuperuser
```

Reload your project in your web browser at

[http://0.0.0.0:8000/](http://0.0.0.0:8000/)

**You should now see the Sharespots website with venues displaying.**

(Optional) Open another browser tab/window and login using the superuser account you created in the django admin panel at [http://0.0.0.0:8000/admin](http://0.0.0.0:8000/admin)

## Front End changes

1. To install [Sass](https://sass-lang.com/install)
   - You can install using node package manager `docker-compose -f local.yml run npm install -g sass`
   - Windows: `choco install sass`
   - Mac OS X: `brew install sass/sass/sass`

2. To build everything Front end related run `npm run build`

## Troubleshooting

If the project doesn't work after pulling the latest changes by doing a `git pull`, you may need to run new database migrations:

```shell
docker-compose -f local.yml run django python manage.py makemigrations
```

## Team

- [Lili](https://github.com/lili2311)
- [Fatimat](https://github.com/gbaja)
- [Maurice](https://github.com/mbanerjeepalmer)
- [Stefano](https://github.com/CianciuStyles)
- [Simon](https://github.com/simonRedwards)
- [Dan](https://github.com/snowkuma)
- [Kit Sum Pang](https://github.com/ktsmpng)
- [Ichi](https://github.com/icicleta)
- [Tsveti](https://github.com/tsvetelinak0)
- [Amy Boyd](https://github.com/amyboyd)
- [Chris Wedgwood](https://github.com/chriswedgwood)
- [Thao Vo](https://github.com/littlethao)
- [Andreea](https://github.com/etiquetteX)
- [Adnan](https://github.com/adnansalehin)
- [Ju-Vern](https://github.com/juvern)
- [Louie Christie](https://github.com/louiechristie)
