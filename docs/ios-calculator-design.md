# iOS Calculator Design Plan

## 1. Overview
This document outlines the UI/UX design specifications for an iOS-style Calculator application. The design closely mirrors the native iOS Calculator, focusing on minimalism, readability, and immediate tactile feedback.

## 2. Layout & Grid
The application follows a strict grid-based layout for the keypad to ensure consistent touch targets and alignment.

*   **Top Section (Display):** 
    *   Takes up approximately the top 30-35% of the screen.
    *   Content is aligned to the bottom-right.
    *   Features dynamic font scaling to accommodate long numbers.
*   **Bottom Section (Keypad):**
    *   Takes up the remaining 65-70% of the screen.
    *   Arranged in a 4-column by 5-row grid.
    *   The "0" button spans two columns (50% width of a normal row) to provide an easy target.
    *   Spacing between buttons is consistent and equal (e.g., 12-16px gap depending on device size).

## 3. Color Palette
The color scheme is designed for high contrast and quick visual recognition of different function types.

*   **Background:** 
    *   Pure Black (`#000000`) for the main app background to blend with the display notch/bezels.
*   **Display Text:** 
    *   Pure White (`#FFFFFF`) for maximum contrast against the black background.
*   **Number Keys (0-9, Decimal):** 
    *   Dark Gray (`#333333`).
    *   Text: White (`#FFFFFF`).
*   **Action Keys (AC, +/-, %):** 
    *   Light Gray (`#A5A5A5`).
    *   Text: Black (`#000000`) for contrast against the light gray.
*   **Operation Keys (÷, ×, -, +, =):** 
    *   Vibrant Orange (`#FF9F0A`).
    *   Text: White (`#FFFFFF`).
    *   *Active State (Operation Selected):* Button becomes White (`#FFFFFF`), and text becomes Orange (`#FF9F0A`).

## 4. Typography
Typography must be clean and highly legible, prioritizing numbers.

*   **Font Family:** San Francisco (SF Pro Display), the default iOS system font.
*   **Display Area:** 
    *   Font Weight: Light or Regular.
    *   Size: Starts very large (e.g., 80pt - 100pt) and scales down as more digits are entered.
*   **Button Text:** 
    *   Font Weight: Medium or Regular.
    *   Size: Standardized large size (e.g., 36pt) to ensure clarity.

## 5. Shape and Touch Targets
*   **Button Shape:** Perfect circles. The "0" button is a horizontal pill shape (stadium) with fully rounded corners.
*   **Touch Targets:** Minimum 44x44 points, though ideally much larger as the buttons should fill the available horizontal width divided by 4, minus the gaps.

## 6. Interaction & Animations
*   **Button Press:** A subtle, quick fade to a lighter shade (for dark gray/orange buttons) or darker shade (for light gray buttons) on touch down, returning to the original color immediately on touch up.
*   **Active Operation:** When an operation (+, -, ×, ÷) is selected, its background smoothly transitions to white, and the icon transitions to orange, holding this state until the next number is pressed or the operation is resolved.
*   **Clear/All Clear:** The "AC" button changes to "C" (Clear) as soon as a user inputs a number, allowing them to clear the current entry without erasing the entire calculation memory.

## 7. Accessibility
*   **Contrast:** Ensure sufficient contrast ratios between text and button backgrounds.
*   **VoiceOver:** Each button must have clear, descriptive accessibility labels (e.g., "Multiply", "Equals", "All Clear").
*   **Dynamic Type:** Support dynamic text sizing for the main display, while keeping button text fixed to maintain grid integrity.
