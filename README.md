## Dependencies

Install required packages:

```bash
pip install "pymongo[srv]" pymongo requests spacy
```
Note: tkinter usually comes pre-installed with Python.

Files
front-end.py
Main file to run the application.
TMDBtoTxt.py
Scrapes movie data (up to ~10,000 movies) from TMDB and stores it in a text file.
MListtoInvertedIndex.py
Converts the movie list into an inverted index.

MDBMongo.py
Uploads movie data to MongoDB.
Format:
```
{ "_id": int, "title": string, "summary": string }
```
InvertedIndextoDB.py
Uploads inverted index data to MongoDB.
Format:
```
{ "_id": int, "keyword": string, "docFreq": int, "mList": [] }
```
