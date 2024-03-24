# 🖥️ Enforcing Minimum Window Size in Flutter Web

Ensuring a minimum window size for your Flutter web application can significantly enhance user experience and maintain design integrity. By implementing a script to enforce a minimum window size in JavaScript, you can prevent users from resizing the window below a specified threshold.

## Implementation Steps:

1. **Create JavaScript Function:**
   Write a JavaScript function to enforce the minimum window size. This function should resize the window back to the minimum dimensions if the user attempts to resize it below the specified threshold.

2. **Attach Function to Window Resize Event:**
   Attach the JavaScript function to the window resize event listener so that it is triggered whenever the window size changes. This ensures consistent enforcement of the minimum size.

3. **Specify Minimum Size:**
   Define the minimum width and height for the window to ensure that the layout remains usable and visually appealing across various devices and screen sizes.

## Example JavaScript Code:

```javascript
<script>
// Define minimum window size
const minWidth = 800;
const minHeight = 600;

// Function to enforce minimum window size
function enforceMinimumSize() {
  if (window.innerWidth < minWidth || window.innerHeight < minHeight) {
    window.resizeTo(
      Math.max(window.innerWidth, minWidth),
      Math.max(window.innerHeight, minHeight)
    );
  }
}

// Attach function to window resize event
window.addEventListener('resize', enforceMinimumSize);

// Call function initially to enforce minimum size on page load
enforceMinimumSize();
</script>

Considerations:
User Experience: 🌟 Enforcing a minimum window size can improve user experience by ensuring that the layout remains usable and visually appealing.

Responsiveness: 📱 Ensure that the minimum window size is compatible with various screen sizes and resolutions to maintain responsiveness.
