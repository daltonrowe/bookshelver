# bookshelver

bookshelver is a lightweight application for organizing a bookshelf by color or lightness.
It takes a series of screenshots via the web browser, camera, API samples, the most vibrant color from each screenshot and stores a list of books in its state.
It then allows users to organize this state by color, lightness other properties.

## Features

### Camera functionality

When clicking the scan book button the browser attempts to use the native camera API to take a picture.
When the picture is taken, it should store a thumbnail of the image at 500x100 pixels JPEG at 0.8 quality stored in state as a base 64 data
When the camera preview is displayed, it should appear as a thumbnail in the bottom center of the screen
Over the thumbnail should be a vertical rectangular outline with an aspect ratio of roughly 5:1.
Tapping or clicking on the video thumbnail will take a snapshot.

### Color extraction

After each snapshot is taken from the camera, the most vibrant color should be selected from the image.
Sample 20 pixels evenly distributed across the image and compare them in the HSL color space.
The pixel with the highest saturation should be selected with a preference towards 50% lightness.
The HSL data should be stored in the state for use by the organizer

### Bookshelf organizer

Each snapshot will appear as a thumbnail in the grid. The grid represents a bookshelf and organizes each snapshot according to its color, grouping similar colors together.
The background color of each element in the grid should be the extracted color from the snapshot. Over top of the background color should be the snapshot image itself at .4 opacity.
Tapping on a snapshot should produce an outline around it with a control panel appearing at the bottom center of the screen.
Each snapshot should be displayed on the shelf as a small item with a five to one aspect.
The grid should wrap to the next row, and 10 books are present

### Control panel (nothing selected)

The control panel should be at the bottom center of the screen and as minimal as possible. It should have a button reading "Scan Book".
Cooking the scan book button attempts to use the devices camera according to the instructions in feature number one.

### Control panel (book selected)

When a book is selected the control panel should show the option to remove that book.

### Control panel (Photo mode)

When the control panel is open and the user is taking a snapshot with their camera, the control panel should show two options.
"Take photo" and "cancel"
