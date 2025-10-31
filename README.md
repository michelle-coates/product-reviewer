# Product Group Reviewer

A browser-compatible React application for reviewing and classifying construction product groups with intelligent similarity matching and batch processing capabilities.

## Features

- **CSV Import/Export**: Load product data from CSV files and export classified results
- **Intelligent Similarity Matching**: Enhanced algorithms that:
  - Filter out size indicators (10LT, 5LT, etc.) and product codes (RAL9003, ND)
  - Give extra weight to important product characteristics (paint finishes, colors, trade terms)
  - Provide boosts for shared paint/coating terminology
- **Batch Processing**: Select multiple similar items and apply the same classification action
- **Real-time Auto-selection**: Automatically pre-select similar items based on adjustable similarity threshold
- **Progress Tracking**: Visual progress bar with completion statistics and streak tracking
- **Local Storage**: Session persistence across browser refreshes
- **Keyboard Shortcuts**: Quick actions with keyboard shortcuts (A, R, U, S, B)

## How to Use

1. **Open the Application**: Simply open `product-reviewer.html` in any modern web browser
2. **Load Data**: Upload a CSV file with columns: `product_id`, `supplier`, `name`, `suggested`, `confidence`
3. **Review Products**: 
   - Use the similarity threshold slider to control auto-selection sensitivity
   - Manually select/deselect similar items for batch processing
   - Choose to Accept, Reassign, mark as Unknown, or Skip each product
4. **Export Results**: Download your classifications as a CSV file

## Technical Details

- **Built with**: React 18, Babel (browser transpilation), PapaParse (CSV), Tailwind CSS
- **Similarity Algorithm**: 
  - 40% TF-IDF scoring with weighted important terms
  - 60% enhanced partial ratio matching with paint-specific boosts
- **Browser Compatibility**: Works in all modern browsers without build tools
- **No Server Required**: Fully client-side application

## Sample Data

The application includes sample construction/building materials data for testing:
- Portland Cement, Oak Hardwood Flooring, Steel Reinforcing Bars
- Bricks, Insulation, Aggregates, Plasterboard, Timber

## Development Notes

This application was developed to handle real-world product classification with particular attention to:
- Paint and coating products with varying brands, finishes, and sizes
- Construction materials with technical specifications
- Bulk processing workflows for efficiency
- User control over automated suggestions

## Recent Enhancements

- Enhanced similarity matching for paint/coating products
- Improved filtering of size indicators and product codes
- Better auto-selection logic that refreshes per product
- Manual override capabilities for all auto-selections
- Paint-specific terminology boosting (trade, matt, white, etc.)
