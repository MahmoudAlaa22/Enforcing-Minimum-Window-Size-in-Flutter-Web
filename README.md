# 🖥️ Enforcing Minimum Window Size in Flutter Web

Ensuring a minimum window size for your Flutter web application can significantly enhance user experience and maintain design integrity. By implementing a script to enforce a minimum window size in JavaScript, you can prevent users from resizing the window below a specified threshold.

## 🛠️ Implementation Steps:

1. **Modify web/index.html:**
   Open your Flutter project and locate the `web/index.html` file. Add a `<script>` tag inside the `<head>` tag or right before the closing `</body>` tag.

2. **Add JavaScript to Disable Inspect:**
   Within the `<script>` tag, insert the following JavaScript code. This code aims to disable right-click and prevent common keyboard shortcuts used for opening developer tools.

## 📝 Example JavaScript Code:

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
```

🤔 Considerations:
User Experience: 🌟 Enforcing a minimum window size can improve user experience by ensuring that the layout remains usable and visually appealing.

Responsiveness: 📱 Ensure that the minimum window size is compatible with various screen sizes and resolutions to maintain responsiveness.
