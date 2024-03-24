# Window-Minimum-Size-Enforcement-Script

# Minimum Size

## Description
The Minimum Size script ensures that the window dimensions meet a specified minimum width and height. It dynamically resizes the window to ensure that it is not smaller than the specified minimum dimensions.

## Usage
1. Include the provided script in your HTML file.
2. Specify the minimum width and height for the window by modifying the `minWidth` and `minHeight` variables in the script.
3. The script will automatically resize the window if its dimensions fall below the specified minimum.

## Example
```html
<!-- Include the script in your HTML file -->
<script>
 function checkWindowSize() {
    // Specify the minimum width and height for the window
    const minWidth = 800;
    const minHeight = 600;

    // Check the current window dimensions
    if (window.innerWidth < minWidth || window.innerHeight < minHeight) {
      // Resize the window to meet the minimum requirements
      window.resizeTo(Math.max(window.innerWidth, minWidth), Math.max(window.innerHeight, minHeight));
    }
  }

  // Add the event listener to the window resize event
  window.addEventListener('resize', checkWindowSize);

  // Call the function initially to ensure the window size meets the requirements
  checkWindowSize();
</script>
