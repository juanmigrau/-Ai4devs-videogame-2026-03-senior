#CONTEXT:
Adopt the role of a senior JavaScript game developer specialized in building interactive browser-based games with clean architecture and efficient state management. Your task is to generate a complete implementation of the classic “Simon Says” memory game that runs in a web browser as a single self-contained HTML file. The game must replicate the core mechanics of Simon: the system generates a sequence of colors and sounds, and the player must repeat the sequence correctly, with increasing difficulty each round.

#GOAL:
Create a fully functional, visually clear, and logically structured Simon game using HTML, CSS, and vanilla JavaScript in one file, ready to run in a browser.

#RESPONSE GUIDELINES:
Follow the step-by-step approach below:

1. Define the core game loop:
   - Initialize an empty sequence array.
   - On each round, append a new random color to the sequence.
   - Play the full sequence to the user with visual and audio feedback.
   - Capture user input and validate it step-by-step against the sequence.

2. Implement game states:
   - “idle” (waiting to start)
   - “playing sequence” (system showing pattern)
   - “user input” (player repeating pattern)
   - “game over”
   Use a clear state variable and prevent invalid interactions between states.

3. Design the UI layout:
   - Create 4 colored buttons (e.g., red, green, blue, yellow) arranged in a grid or circle.
   - Add a start button and score display.
   - Include a visual feedback effect (e.g., brightness change or animation) when a color is activated.

4. Add sound integration:
   - Assign a unique tone to each color using the Web Audio API or simple audio objects.
   - Ensure sounds play both during system playback and user input.

5. Handle user interaction:
   - Capture clicks on color buttons.
   - Store user inputs in order.
   - Compare each input immediately with the sequence.
   - If incorrect → trigger game over.
   - If correct and sequence complete → advance to next round after delay.

6. Implement progression mechanics:
   - Increase sequence length by 1 each round.
   - Optionally reduce delay between steps to increase difficulty.
   - Update score based on rounds completed.

7. Add game over handling:
   - Display a clear “Game Over” message.
   - Show final score.
   - Reset state so the player can restart.

8. Code structure and readability:
   - Organize code into logical functions (e.g., playSequence, handleUserInput, nextRound).
   - Use comments to explain key logic blocks.
   - Avoid global clutter by grouping related variables.

9. Styling:
   - Use simple but high-contrast colors.
   - Ensure buttons are large and responsive.
   - Center the game on screen and make it usable on different screen sizes.

#INFORMATION ABOUT ME:
- My preferred color set: red, blue, yellow and green
- My difficulty scaling preference (fixed speed / increasing speed): fixed speed
- My sound preference (simple tones / custom audio files): simple tones
- My UI style preference (minimal / arcade / modern): arcade
- My starting sequence length: 3

#OUTPUT:
Produce a single HTML file containing:
- All HTML structure
- Inline CSS inside <style> tags
- Inline JavaScript inside <script> tags

The output must:
- Run immediately when opened in a browser
- Include clear inline comments explaining the logic
- Fully implement the Simon game mechanics described
- Avoid external libraries or dependencies
- Be cleanly formatted and easy to modify

Return ONLY the full HTML code.
