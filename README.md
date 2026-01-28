# Academic Pulse - Student Transcript Visualizer

An interactive data visualization tool that transforms student transcripts into compelling visual insights using Chart.js.

## Features

- **Multiple File Format Support**: Upload JSON or PDF transcripts
- **Interactive Charts**: 
  - GPA progression line chart
  - Grade distribution doughnut chart
  - Subject performance bar chart
  - Detailed course history
- **Automatic Analysis**:
  - GPA calculations with trend indicators
  - Subject-level performance metrics
  - Semester-by-semester breakdown
- **Responsive Design**: Works seamlessly on desktop and mobile devices

## How to Use

1. **Open** `transcript-visualizer.html` in any modern web browser
2. **Upload** your transcript file:
   - Drag and drop a file onto the upload zone, OR
   - Click "Choose File" to browse, OR
   - Click "Load Sample Data" to see an example
3. **View** your interactive visualizations instantly

## Supported File Formats

### JSON Format
For best results, use a JSON file with the following structure:

```json
{
  "student": {
    "name": "Student Name",
    "id": "12345",
    "major": "Your Major",
    "enrollment_date": "2021-09-01"
  },
  "courses": [
    {
      "code": "CS101",
      "name": "Course Name",
      "credits": 4,
      "grade": "A",
      "semester": "Fall 2021",
      "gpa_points": 4.0
    }
  ]
}
```

**Field Descriptions:**
- `code`: Course code (e.g., "CS101", "MATH201")
- `name`: Full course name
- `credits`: Number of credit hours (typically 1-6)
- `grade`: Letter grade (A+, A, A-, B+, B, B-, C+, C, C-, D+, D, D-, F)
- `semester`: Semester taken (e.g., "Fall 2021", "Spring 2022")
- `gpa_points`: GPA value for the grade (4.0 scale)

### PDF Format
Upload a PDF transcript with:
- Student information (name, ID, major)
- Course listings with codes, names, credits, and grades
- Semester/term information

The tool automatically extracts and parses text from PDFs. For best results, ensure your PDF:
- Contains readable text (not scanned images)
- Follows a standard transcript format
- Includes course codes, grades, and credit hours

**Common PDF Formats Supported:**
- University official transcripts
- Course listings with tabular data
- Academic records with semester breakdowns

## Technical Details

**Technologies Used:**
- Chart.js 4.4.0 for data visualizations
- PDF.js 3.11.174 for PDF text extraction
- Pure JavaScript (no frameworks required)
- Responsive CSS with modern animations

**Browser Compatibility:**
- Chrome/Edge (recommended)
- Firefox
- Safari
- Any modern browser with ES6 support

## Files Included

1. `transcript-visualizer.html` - Main application (open this file)
2. `sample-transcript.json` - Example JSON data
3. `sample-transcript.pdf` - Example PDF transcript
4. `README.md` - This documentation

## Customization

To customize the visualizer:
- Modify CSS variables in the `:root` selector for colors
- Adjust chart configurations in the visualization functions
- Add new metrics or calculations in the `visualizeData()` function

## Troubleshooting

**PDF not parsing correctly?**
- Ensure the PDF contains selectable text (not a scanned image)
- Try using the JSON format for more reliable results
- Check that your PDF follows a standard transcript format

**Charts not displaying?**
- Ensure you have an internet connection (for Chart.js CDN)
- Check browser console for any errors
- Try a different browser

**Need help?**
Click "Load Sample Data" to see a working example of the expected format.

## Data Privacy

All processing happens locally in your browser. No data is uploaded to any server.

---

Created with Chart.js • Designed for students and educators
