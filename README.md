# JOURney Journal Cover Voting

This project is a web-based ranked-choice voting system designed for selecting the cover for the JOURney Journal. Users can drag and drop cover images to rank them according to their preference. The interface displays covers in a responsive two-column grid with a modal lightbox for a closer look, and it prevents duplicate submissions.

## Features

- **Ranked-Choice Voting:** Drag and drop covers to order them by preference.
- **Two-Column Grid Layout:** Portrait images are shown side by side for a balanced design.
- **Centered Content:** Each cover is centered both horizontally and vertically within its box.
- **Modal Lightbox:** Click on a cover to enlarge and inspect it in detail.
- **Random Order:** Covers appear in a random order on every page load.
- **Duplicate Prevention:** Prevents multiple submissions by the same user (based on first and last name).
- **Google Sheets Integration:** Votes are sent to and recorded in a Google Sheet via a Google Apps Script web app.

## Setup & Deployment

1. **Clone the Repository:**
       ```bash
       git clone https://github.com/rmharp/JOURneyCover.git
       cd your-repository
       ```

3. **Optimize and Upload Images:**
   - Place your cover images (`cover1.jpg` through `cover24.jpg`) in the `./media/` folder.
   - Use an image compression tool (like [TinyPNG](https://tinypng.com/)) if needed.

4. **Configure Google Apps Script:**
   - Create a new Google Apps Script project.
   - Copy the provided backend code (with `doPost` and `doGet` functions) into the script.
   - Deploy the script as a web app with access set to "Anyone, even anonymous."
   - Update the `scriptURL` in the HTML file with the deployed web app URL.

5. **Deploy via GitHub Pages:**
   - Commit your changes:
           ```bash
           git add .
           git commit -m "Initial commit for JOURney Journal Cover Voting"
           git push origin main
           ```

   - Enable GitHub Pages in your repository settings.

6. **Test Your Application:**
   - Open your GitHub Pages URL.
   - Verify that the covers appear in a two-column grid, can be reordered, and that clicking on a cover opens an enlarged view.
   - Submit a vote to confirm that data is recorded in your Google Sheet.

## Technologies Used

- HTML5, CSS3, and JavaScript
- [SortableJS](https://github.com/SortableJS/Sortable) for drag-and-drop functionality
- Google Apps Script for backend integration with Google Sheets
- Git and GitHub Pages for deployment
