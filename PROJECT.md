# bookshelver

bookshelver is a lightweight application for organizing a bookshelf by color or lightness.
It takes a series of screenshots via the web browser, camera, API samples, the most vibrant color from each screenshot and stores a list of books in its state.
It then allows users to organize this state by color, lightness other properties.

## Features

1. Camera functionality

When clicking the scan book button the browser attempts to use the native camera API to take a picture.
When the picture is taken, it should store a thumbnail of the image at 500x500 pixels JPEG at 0.8 quality stored in state as a base 64 data URL.
