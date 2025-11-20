# MC Scanner

A very simple web-based tool for creating and marking Multiple Choice (MC) answer sheets. Perfect for teachers without budget—completely free, no installation, no complexity. Just open and use.

This tool allows manual marking by scanning answer sheets (camera optional), which is ideal when students erase and change their answers—unlike automated scanners that may struggle with erasures.

**Live Demo**: [https://mc-scanner.surge.sh](https://mc-scanner.surge.sh)

## Features

- **Configurable Questions**: Set the total number of questions and questions per table
- **Manual Marking**: Click on A, B, C, or D options to mark answers manually—ideal when students erase and change answers
- **Auto-Save**: All answers and settings are automatically saved to browser localStorage—no data loss on accidental refresh
- **Clear Function**: Clear all answers with one click while preserving your settings
- **Optional Camera Support**: Use your device's camera to scan answer sheets (useful for mobile devices)
- **Data Export**: Share or copy your answers as JSON data
- **Responsive Design**: Works on desktop and mobile devices

## Usage

All answers and settings are automatically saved—no need to worry about accidental page refreshes.

1. **Set Total Questions**: Enter the total number of questions in the "Total Questions" field
2. **Set Questions per Table**: Configure how many questions appear in each table
3. **Mark Answers**: Click on the A, B, C, or D cell for each question to mark the answer
4. **Optional Camera**: Click "Start Camera" to overlay the camera view on the answer sheet for easier scanning
5. **Clear Answers**: Click "Clear" to remove all answer marks (settings are preserved)
6. **Export Data**:
   - Click "Share" to share the data using the Web Share API
   - Click "Copy" to copy the JSON data to your clipboard

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

- A modern web browser with JavaScript enabled
- For optional camera functionality: A device with a camera and browser support for `getUserMedia` API

## License

This project is licensed with [BSD-2-Clause](./LICENSE)

This is free, libre, and open-source software. It comes down to four essential freedoms [[ref]](https://seirdy.one/2021/01/27/whatsapp-and-the-domestication-of-users.html#fnref:2):

- The freedom to run the program as you wish, for any purpose
- The freedom to study how the program works, and change it so it does your computing as you wish
- The freedom to redistribute copies so you can help others
- The freedom to distribute copies of your modified versions to others
