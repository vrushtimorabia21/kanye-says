# Kanye Says...

A simple Python desktop app built with Tkinter. Click Kanye's face and the app fetches a random quote from the [Kanye.rest](https://kanye.rest/) API, then displays it on a custom background. It's a fun beginner project for practicing GUI design, API calls, JSON parsing, and handling button events in Python.

## Features

- Tkinter GUI with a custom background image
- Fetches a random quote from the Kanye.rest API on each click
- Updates the quote text on the canvas without reopening the window

## Requirements

- Python 3.x
- [`requests`](https://pypi.org/project/requests/)
- Tkinter (included with most Python installations)

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/your-username/kanye-says.git
   cd kanye-says
   ```

2. Install the dependency:

   ```bash
   pip install requests
   ```

3. Make sure these image files are in the same folder as the script:

   - `background.png` (the quote background, sized around 300x414)
   - `kanye.png` (the button image)

## Usage

Run the app:

```bash
python main.py
```

Then click the Kanye image to get a new quote.

## Project Structure

```
kanye-says/
├── main.py
├── background.png
├── kanye.png
└── README.md
```

## How It Works

1. The button's `command` calls `get_quote()`.
2. `get_quote()` sends a GET request to `https://api.kanye.rest/`.
3. The JSON response is parsed and the `quote` field is extracted.
4. The canvas text item is updated with `canvas.itemconfig()`.

## Concepts Practiced

- Building GUIs with Tkinter (`Canvas`, `Button`, `PhotoImage`)
- Making HTTP requests and handling errors with `requests`
- Parsing JSON data
- Event-driven programming

## Credits

- Quotes provided by the free [Kanye.rest](https://kanye.rest/) API

## License

This project is open source and available under the [MIT License](LICENSE).
