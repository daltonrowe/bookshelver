# bookshelver

bookshelver is a lightweight application for organizing a bookshelf by color or lightness.
It takes a series of screenshots via the web browser camera API, and sample the most vibrant color from each screenshot and stores a list of books in its state.
It then allows users to organize this state by color.

## Features

### Camera functionality

When clicking the scan book button the browser attempts to use the native camera API to take a picture.
When the picture is taken, it should store a thumbnail of the image at 100x500 pixels JPEG at 0.8 quality stored in state as a base64 data url
When the camera preview is displayed, it should appear as a thumbnail directly above the control panel, in the bottom middle of the screen
Over the thumbnail should be a vertical rectangular outline with an aspect ratio of roughly 1:5.
Tapping or clicking on the video thumbnail will take a snapshot.

### Color extraction

After each snapshot is taken from the camera, the most vibrant color should be selected from the image.
Sample 20 pixels evenly distributed across the image and compare them in the HSL color space.
The pixel with the highest saturation should be selected with a preference towards 70% lightness being the tiebreaker.
The HSL data should be stored in the state for use by the organizer.

### Bookshelf organizer

Each snapshot will appear as a thumbnail in the grid. The grid represents a bookshelf and organizes each snapshot according to its color, grouping similar colors together.
The background color of each element in the grid should be the extracted color from the snapshot.
Over top of the background color should be the snapshot image itself at .2 opacity with CSS blend mode of multiply.

Tapping on a snapshot should produce an outline around it with a control panel appearing at the bottom center of the screen.
Each snapshot should be displayed on the shelf as a small item with a 1:5 aspect ratio.
The grid should wrap to the next row when 10 books are present, or according to the wrap value set in the control panel.

### Control panel (nothing selected)

The control panel should be at the bottom center of the screen and as minimal as possible.
It should have a button reading "Scan Book", and number input controlling the wrap value (number of books per row) with a default of 10.
Clicking the scan book button attempts to use the device's camera according to the instructions in feature number one.

### Control panel (book selected)

When a book is selected the control panel should show the option to remove that book.

### Control panel (Photo mode)

When the control panel is open and the user is taking a snapshot with their camera, the control panel should show two options.
"Take photo" and "cancel"
When in photo mode the camera preview should appear above the control panel.
Taking a photo should not close the photo preview, allowing the user to take multiple snapshots in a row.
