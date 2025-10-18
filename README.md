# Presentation Generator - Quick Start

## Setup Instructions

1. **Create Google Spreadsheet**
   - Create new Google Spreadsheet
   - Create sheet named "Slides" → Import `slides.csv`
   - Create sheet named "Config" → Import `config.csv`

2. **Add Generator Script**
   - In Google Sheets: Extensions → Apps Script
   - Delete default code
   - Copy all content from `generator.js`
   - Save (Ctrl+S or Cmd+S)
   - Refresh the spreadsheet

3. **Generate Presentation**
   - Use menu: Presentation Generator → Generate Presentation
   - Find your new presentation in Google Drive

## File Structure

```
your-presentation/
├── slides.csv      # Your slide content
├── config.csv      # Presentation settings
├── generator.js    # Google Apps Script
├── chart_prompts.md  # Templates for chart generation
├── version.json    # Version tracking
└── README.md       # This file
```

## Customization Guide

### Adding Slides
Edit `slides.csv` to add new slides. Key columns:
- `order`: Slide sequence number
- `section_id`: S1, S2, etc. for sections
- `layout`: Title, Content, Section, TwoColumn
- `title`: Slide title
- `subtitle`: Optional subtitle
- `bullets`: Main content (use • for bullet points)
- `speaker_notes`: Presenter notes

### Layout Types
- **Title**: Opening slide
- **Section**: Section dividers
- **Content**: Standard bullet slides
- **TwoColumn**: Side-by-side content (use | to separate)

### Configuration
Edit `config.csv` to change:
- **deck_title**: Base presentation title
- **company**: Company name (optional - will prefix title as `[Company] Title`)
- **presenter_name**: Your name
- **presentation_date**: Date of presentation
- Duration and timing settings
- Visual styling (theme colors, fonts)

**Note:** Generated presentations automatically include timestamps (e.g., `Title - YYYY-MM-DD HH:mm`) for easy version tracking. If you include a company name, it will be prefixed to the title.

## Quick Tips

1. **Use pipe (|) as delimiter** when importing CSV
2. **Keep bullets concise** - expand in speaker notes
3. **Test with few slides first** before full generation
4. **Check slide order numbers** - they control sequence

## Working with Claude

When working with Claude on this presentation:
1. Share the CSV files for content editing
2. Ask Claude to help structure your content
3. Use Claude to generate speaker notes
4. Request specific slide layouts or sections
5. Use chart_prompts.md to generate custom charts

## Advanced Features

The system includes several advanced capabilities:
- **GitHub Integration**: Auto-update from repositories (see generator.js GITHUB_CONFIG)
- **Version Tracking**: Semantic versioning via version.json
- **Backup System**: Automatic backups before updates
- **Image/Chart Insertion**: Insert media from Google Drive
- **Validation Tools**: Test and validate your slide data

Start simple with basic slides, then add advanced features as needed!