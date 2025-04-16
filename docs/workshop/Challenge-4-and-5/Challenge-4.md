# Workshop Challenge: Changing the Logo in the App

One of the easiest and most fun changes you can make to the app is updating the logo! Follow these step-by-step instructions to replace the current logo with your own.

---

## **Step 1: Prepare Your New Logo**
1. Create or find the logo you want to use.
2. Save the logo as an image file (e.g., `logo.png`).
3. Ensure the image has a reasonable size (e.g., 100x100 pixels) for better display.

---

## **Step 2: Add the Logo to the Project**
1. Navigate to the `src/components/Svg` folder in your project directory.
2. Replace the existing logo file or add your new logo file to this folder.
   - Example: Save your new logo as `NewLogo.png`.

---

## **Step 3: Update the Logo Component**
1. Open the `AppLogo` component file:
   - Filepath: `src/components/Svg/Svg.tsx`.
2. Locate the current logo implementation. It might look like this:

```tsx
export const AppLogo: React.FC = () => (
    <img src="/path/to/current/logo.png" alt="App Logo" />
);