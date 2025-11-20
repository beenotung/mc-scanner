# MC Scanner

A simple web tool for marking Multiple Choice answer sheets. Perfect for teachers without budget—completely free, no installation needed.

**Live Demo**: [https://mc-scanner.surge.sh](https://mc-scanner.surge.sh)

Manual marking by scanning answer sheets (camera optional). Ideal when students erase and change answers—unlike automated scanners that struggle with erasures.

## Features

- **Configurable**: Set total questions and questions per table
- **Auto-Save**: All answers and settings saved automatically—no data loss on refresh
- **Manual Marking**: Click A, B, C, or D to mark answers
- **Camera Support**: Optional camera overlay for scanning (mobile-friendly)
- **Export**: Share or copy answers as JSON
- **Responsive**: Works on desktop and mobile

## Usage

1. Set total questions and questions per table
2. Click A, B, C, or D to mark answers (auto-saved)
3. Optional: Use camera overlay for easier scanning
4. Export: Share or copy answers as JSON
5. Clear: Remove all marks (settings preserved)

## Data Format

The exported data is in JSON format:

```json
{
  "seat": "seat_number",
  "answers": [
    { "id": 1, "option": 1 },
    { "id": 2, "option": 2 },
    ...
  ]
}
```

Where:

- `seat`: The seat number (entered when exporting)
- `answers`: Array of answer objects
  - `id`: Question number
  - `option`: Selected option (1=A, 2=B, 3=C, 4=D, 0=no answer)

## Requirements

- Modern web browser with JavaScript
- Camera (optional): Device with camera and `getUserMedia` API support

## License

This project is licensed with [BSD-2-Clause](./LICENSE)

This is free, libre, and open-source software. It comes down to four essential freedoms [[ref]](https://seirdy.one/2021/01/27/whatsapp-and-the-domestication-of-users.html#fnref:2):

- The freedom to run the program as you wish, for any purpose
- The freedom to study how the program works, and change it so it does your computing as you wish
- The freedom to redistribute copies so you can help others
- The freedom to distribute copies of your modified versions to others
