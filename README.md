# TMDB Movie CLI program

A simple Python CLI tool that fetches movie lists from **The Movie Database (TMDB)** using the `/movie/now_playing`, `/popular`, `/top_rated`, and `/upcoming` endpoints.

It retrieves data from the TMDB API and prints basic movie information in the terminal.

---

## Overview

This script queries the TMDB API and displays a list of movies based on a selected category:

* Now Playing
* Popular
* Top Rated
* Upcoming

It is intentionally minimal and primarily demonstrates:

* Basic API consumption
* CLI argument parsing
* Use of Bearer token authentication

---

## Authentication

This project requires a **TMDB Bearer token**.

When the script runs, it prompts:

```
Enter your bearer token:
```

The token is:

* Required for all requests
* Hidden during input (via `getpass`)
* Sent using the `Authorization: Bearer <token>` header

---

## Concepts Demonstrated

* REST API requests using requests
* Bearer token authentication via HTTP headers
* CLI argument parsing with argparse
* Basic JSON parsing
* Simple control flow using match/case

---

## Requirements

* Python 3.10+
* `requests` library
* A valid TMDB API Bearer token

Install dependency:

```
pip install requests
```

---

## Installation

1. Clone the repository:

```
git clone https://github.com/tfowl95/tmdb-movie-listings.git
cd tmdb-movie-listings
```

2. Add to PATH

3. Make executable (macOS/Linux):

```
chmod +x tmdb-list
```

---

## Usage

Run the script with one of the supported movie categories:

```
tmdb-list playing
tmdb-list popular
tmdb-list top
tmdb-list upcoming
```

---

## Example Output

```
----------------------
Dune: Part Two
Paul Atreides unites with the Fremen...
Avg rating: 8.4
----------------------
Kung Fu Panda 4
Po must train a new Dragon Warrior...
Avg rating: 7.1
----------------------
```

---

## Notes

* This script does not cache responses
* No pagination handling is implemented (only first page returned)
* Requires a valid TMDB API token on each run
* Intended for learning / CLI experimentation, not production use

---

## License

No license specified.
