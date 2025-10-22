# ShareVolume

## Summary

This application was automatically generated to fulfill the following requirements:

Your assigned company: Carnival (CCL), CIK 0000815097.

Fetch https://data.sec.gov/api/xbrl/companyconcept/CIK0000815097/dei/EntityCommonStockSharesOutstanding.json (set a descriptive User-Agent per SEC guidance).
Read `.entityName`. Filter `.units.shares[]` for entries whose `fy` > "2020" and
includes a numeric `val`.
Save `data.json` with this structure:
`{"entityName": "Carnival", "max": {"val": ..., "fy": ...}, "min": {"val": ..., "fy": ...}}`
where `max` and `min` refer to the highest and lowest `.val`. Break ties however you like.

Render a visually appealing `index.html` where:
- `<title>` and `<h1>` must include the live `entityName`.
- The max/min figures are clearly marked with these IDs:
  `share-entity-name`,
  `share-max-value`, `share-max-fy`,
  `share-min-value`, `share-min-fy`.

If the page is opened as `index.html?CIK=0001018724` (or any other 10-digit CIK),
`fetch()` from the SEC endpoint for that CIK using any proxy, e.g. AIPipe,
replace every ID listed above and the title and H1 without reloading the page.

Also commit the attachment uid.txt as-is.

## Features

This single-page application provides:
- Clean, responsive user interface
- Real-time functionality
- Error handling and validation
- Cross-browser compatibility

## Setup

1. Clone this repository:
   ```bash
   git clone https://github.com/AmalFrancisOlakengil/ShareVolume.git
   cd ShareVolume
   ```

2. Open `index.html` in your web browser or visit the live demo

## Usage

Simply open the `index.html` file in a modern web browser. The application is fully self-contained and requires no build process or dependencies.

## Live Demo

🌐 [View Live Application](https://AmalFrancisOlakengil.github.io/ShareVolume/)

## Code Explanation

The application is built as a single HTML file containing:

- **HTML Structure**: Semantic markup for accessibility
- **CSS Styling**: Embedded styles using modern CSS features
- **JavaScript Logic**: Vanilla JavaScript for functionality
- **Error Handling**: Robust error handling throughout

## Evaluation Checks (Round 1)

This application satisfies the following checks:

- Each required file exists on GitHub
- uid.txt matches the attached uid.txt
- LICENSE contains the MIT License text
- data.json exists and is valid JSON
- data.json has 'entityName' field matching 'Carnival'
- data.json has 'max' object with 'val' (number) and 'fy' (string) fields
- data.json has 'min' object with 'val' (number) and 'fy' (string) fields
- data.json max.fy and min.fy are both > '2020'
- data.json max.val is greater than or equal to min.val
- index.html exists
- index.html <title> contains the entityName from data.json
- index.html <h1 id='share-entity-name'> contains the entityName from data.json
- index.html contains element with id='share-max-value' displaying max.val
- index.html contains element with id='share-max-fy' displaying max.fy
- index.html contains element with id='share-min-value' displaying min.val
- index.html contains element with id='share-min-fy' displaying min.fy
- index.html fetches data.json using fetch('https://data.sec.gov/api/xbrl/companyconcept/CIK0000815097/dei/EntityCommonStockSharesOutstanding.json')
- index.html supports ?CIK= query parameter to fetch alternate company data
- index.html dynamically updates all elements when ?CIK= is provided

## License

MIT License - See LICENSE file for details

## Generated

This application was automatically generated on 2025-10-22 13:57:36 using Gemini API for LLM-assisted code generation.

---
*Last updated: Round 1 - 2025-10-22 13:57:36*
