# Curious Studio Website Guidelines

## Overview
- Educational studio called **Curious Studio**
- Goal: Introduce services and who we are

## Home Page
- **No header image** on home page
- Simple introduction: "**Curious Studio** is a creative space where children build confidence, nurture curiosity, and discover the joy of making."
- Two primary navigation buttons: "Programs" and "Books"

## Navigation Structure
- **Top Navigation Menu**: Programs, Books, About (always visible)
- **Home**: Landing page with hero image, intro, and navigation buttons
- **Programs**: Shows program listing and details
  - **Young Artists Studio**: First program (detailed content)
  - Future programs will be added here
- **Books**: (To be developed)
- **About**: About Curious Studio page with mission, approach, and contact info

## User Authentication
- **Log In / Sign Up**: Button in top right corner
- Users must be logged in to book programs
- After login, users can:
  - Book programs through "Check Availability"
  - View enrolled programs in "My Programs"
  - Access user menu with dropdown (My Programs, Log Out)
- User data stored in browser localStorage (demo implementation)

## Programs Page Content Requirements
- When user clicks "Programs" button, display program page
- Young Artists Studio shows as the first program
- Structure designed to accommodate multiple programs in the future

### Young Artists Studio
The page should inform parents about:
1. What the program is (ages 4-6, 45 minutes, San Diego)
2. Who it's for (eligibility criteria)
3. What happens in class (class flow and activities)
4. Teaching principles
5. Why art matters (developmental benefits)
6. About the instructor

### Call to Action
- **Primary CTA**: "Check Availability"
- **Placement**: Top right of navigation AND bottom of program page
- **Functionality**: When clicked, parents select the week to see available spots

## Visual Design Guidelines

### Color Palette
- **Primary Color**: #00B469 (green) - use for primary buttons
- **Accent Range**: Green to yellow-green spectrum
- **Goal**: Bright, positive look and feel
- **Important**: Keep it simple, avoid looking too childish
- Use ONLY ONE accent color (green)

### Design Philosophy
- Follow Apple HCI (Human-Computer Interaction) guidelines for web design
- Bright look while maintaining simplicity
- Professional yet approachable
- Clean, modern aesthetic

### Usability Requirements
- All fonts must be usability-safe
- All visuals must be usability-safe
- Ensure accessibility and readability

## Technical Requirements
- **Main file**: index.html
- **Stylesheet**: styles.css (or style.css)
- CSS file must be properly linked to index.html
- Save files in the project folder
