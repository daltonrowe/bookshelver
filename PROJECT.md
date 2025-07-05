# bookshelver

bookshelver is a lightweight application for organizing a bookshelf by color or lightness.
It takes a series of screenshots via the web browser, camera, API samples, the most vibrant color from each screenshot and stores a list of books in its state.
It then allows users to organize this state by color, lightness other properties.

## Features

1. Camera functionality

When clicking the scan book button the browser attempts to use the native camera API to take a picture.
When the picture is taken, it should store a thumbnail of the image at 500x500 pixels JPEG at 0.8 quality stored in state as a base 64 data
When the camera preview is displayed, it should appear as a thumbnail in the bottom center of the screen
Over the thumbnail should be a rectangular outline with an aspect ratio of roughly 5 to one in a vertical orientation.
Tapping or clicking on the video thumbnail will take a snapshot.

2. Bookshelf organizer

Each snapshot will appear as a thumbnail in the grid. The grid represents a bookshelf and organizes each snapshot according to its color, grouping similar colors together.
The background color of each element in the grid should be the extracted color from the snapshot. Over top of the background color should be the snapshot image itself at .4 opacity.
Tapping on a snapshot should produce an outline around it with a control panel appearing at the bottom center of the screen.

3. Control panel (nothing selected)

The control panel should be at the bottom center of the screen and as minimal as possible. It should have a button reading "Scan Book".
Cooking the scan book button attempts to use the devices camera according to the instructions in feature number one.

4. Control panel (book selected)

When a book is selected the control panel should show the option to remove that book.
