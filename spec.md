Let's write a single-page vue app allowing the user to mockup screenshots (and whatever else), using a 9 slice approach.
[index](index.html) already contains some boilerplate and cdn setup.

For now, simply allow the user to upload an image, and dynamically load `mocks/list.txt` (each line is the name of an available mock) and let the user choose which mock they want to use, then allow downloading the resulting image.

in `mocks/spec/$name.txt`, we always find the relevant data for a given mock.
First line is the name of the mock image, path always `mocks/img`, then follow 4 lines with 9-slice info, to be interpreted like `border-image-slice` prop in CSS (top, right, bottom, left is the order).