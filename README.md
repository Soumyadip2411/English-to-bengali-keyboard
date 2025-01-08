# Bengali Keyboard Mapper

This Python project uses the `keyboard` library to create a custom keyboard layout that maps English characters to their corresponding Bengali characters. It listens for key presses and writes Bengali characters when specific English keys are pressed.

## Features
- **Custom Mapping**: English characters are mapped to Bengali characters via a `map.txt` file.
- **Ctrl Key Support**: The `Ctrl` key is used to enable special key combinations.
- **Dynamic Key Events**: The script listens for key press and release events and processes them accordingly.
- **Quit on ESC**: The script stops when the `ESC` key is pressed.

## Installation

1. Clone this repository to your local machine:
    ```bash
    git clone https://github.com/yourusername/bengali-keyboard-mapper.git
    cd bengali-keyboard-mapper
    ```

2. Install the required dependencies:
    ```bash
    pip install keyboard
    ```

3. Make sure the `map.txt` file is available in the project folder with the following structure:
    ```
    a: অ
    b: ব
    c: চ
    ...
    ```

## How to Use

1. **Run the script**:
    ```bash
    python bengali_mapper.py
    ```

2. **Map File**:
    - The `map.txt` file contains a list of English-to-Bengali character mappings, one per line.
    - Format: `EnglishChar:BengaliChar`, for example: `a:অ`.
    - The file must be saved in UTF-8 encoding.

3. **Control Mechanism**:
    - Use **Ctrl** to enable special key combinations (e.g., pressing Ctrl+key for Bengali characters).

4. **Quit the script**:
    - Press the **ESC** key to stop the script.

## Code Workflow

- The script listens for key press and release events using the `keyboard` library.
- When an English character is pressed, it checks if it is mapped to a Bengali character (from the `map.txt` file).
- If the key is found in the mapping, the corresponding Bengali character is typed.
- If the key is not found in the mapping, the character is pressed as-is.

## License

This project is open-source and available under the [MIT License](LICENSE).
