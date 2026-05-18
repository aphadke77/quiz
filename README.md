# Interactive Quiz Web Application

A fully functional, interactive quiz application built with vanilla HTML, CSS, and JavaScript. Features local storage database for persisting quiz results and tracking user progress.

## Features

### 📝 Quiz Functionality

- **10 Web Development Questions** - Multiple-choice questions covering HTML, CSS, and JavaScript
- **Progress Tracking** - Visual progress bar showing quiz completion status
- **Navigation** - Move back and forth between questions before submitting
- **Timer** - Tracks time taken to complete the quiz
- **Answer Selection** - Click to select answers with visual feedback

### 💾 Local Storage Database

- **Automatic Saving** - Quiz results are automatically saved to browser’s local storage
- **Persistent Data** - Results remain available even after closing the browser
- **History Tracking** - View all previous quiz attempts with scores and times
- **Data Management** - Option to clear history when needed

### 📊 Results & Analytics

- **Score Calculation** - Instant percentage-based scoring
- **Question Review** - See which questions were answered correctly/incorrectly
- **Time Tracking** - View completion time for each attempt
- **History Comparison** - Compare scores across multiple attempts

### 🎨 User Interface

- **Responsive Design** - Works seamlessly on desktop, tablet, and mobile devices
- **Modern Styling** - Clean, professional interface with smooth animations
- **Color-Coded Feedback** - Visual indicators for correct/incorrect answers
- **Intuitive Controls** - Easy-to-use navigation buttons

## Installation

### Option 1: Direct Use

1. Save the HTML file to your computer
1. Open the file in any modern web browser
1. Start taking the quiz immediately

### Option 2: Web Server

1. Place the HTML file in your web server’s public directory
1. Access it through your web server URL
1. Share with multiple users

## Usage Guide

### Taking a Quiz

1. **Start**: Open the application in your browser - the quiz begins automatically
1. **Answer Questions**:
- Click on your chosen answer for each question
- Selected answers are highlighted in blue
1. **Navigate**:
- Use “Previous” button to review earlier questions
- Use “Next” button to move forward
- Change answers at any time before finishing
1. **Complete**: After answering the final question, click “Next” to submit

### Viewing Results

After completing the quiz, you’ll see:

- Your overall score as a percentage
- A detailed breakdown of each question
- Correct/incorrect indicators for each answer
- Total time taken to complete the quiz

### Accessing History

1. Click **“View History”** button on the results page
1. See all previous quiz attempts sorted by date
1. Compare scores and completion times
1. Click **“Clear History”** to remove all saved attempts (requires confirmation)

### Retaking the Quiz

- Click **“Retake Quiz”** button to start a fresh attempt
- Previous results are saved in history
- Timer and progress reset automatically

## Technical Details

### Technologies Used

- **HTML5** - Structure and semantic markup
- **CSS3** - Styling, animations, and responsive design
- **JavaScript (ES6+)** - Application logic and interactivity
- **LocalStorage API** - Client-side data persistence

### Browser Compatibility

- ✅ Chrome/Edge (latest)
- ✅ Firefox (latest)
- ✅ Safari (latest)
- ✅ Opera (latest)
- ⚠️ Internet Explorer (not supported)

### Data Storage Structure

Quiz results are stored in LocalStorage with the following structure:

```javascript
{
  "quizHistory": [
    {
      "date": "5/18/2026, 10:30:45 AM",
      "score": 80,
      "time": "02:15",
      "answers": [0, 1, 2, 3, 1, 0, 2, 1, 0, 3]
    }
  ]
}
```

### Local Storage Limits

- Maximum storage: ~5-10MB (varies by browser)
- Estimated capacity: ~1000+ quiz attempts
- Data persists until manually cleared or browser cache is cleared

## Customization

### Adding/Modifying Questions

Edit the `quizData` array in the JavaScript section:

```javascript
const quizData = [
    {
        question: "Your question here?",
        options: ["Option 1", "Option 2", "Option 3", "Option 4"],
        answer: 0  // Index of correct answer (0-3)
    },
    // Add more questions...
];
```

### Changing Colors

Modify CSS variables in the `:root` selector:

```css
:root {
    --primary-color: #4361ee;      /* Main theme color */
    --secondary-color: #3a0ca3;    /* Secondary accents */
    --success-color: #4cc9f0;      /* Correct answers */
    --danger-color: #f72585;       /* Incorrect answers */
}
```

### Adjusting Timer

The timer starts automatically when the quiz begins and stops when submitted. To disable:

```javascript
// Comment out these lines in initQuiz():
// startTimer();

// And in finishQuiz():
// clearInterval(timerInterval);
```

## Features in Detail

### Progress Bar

- Updates automatically as you move through questions
- Shows percentage of quiz completion
- Smooth animation transitions

### Answer Validation

- Prevents skipping questions without answering
- “Next” button disabled until an answer is selected
- Visual confirmation of selected answers

### Responsive Design

- Adapts to screen sizes from 320px to 4K
- Touch-friendly buttons on mobile devices
- Optimized layout for tablets

## Privacy & Data

- **100% Client-Side** - No data sent to external servers
- **Local Only** - All data stored in your browser
- **User Control** - Clear your data anytime
- **No Tracking** - No analytics or cookies

## Troubleshooting

### Quiz Not Loading

- Ensure JavaScript is enabled in your browser
- Check browser console for errors (F12)
- Try clearing browser cache

### History Not Saving

- Check if LocalStorage is enabled
- Verify sufficient storage space
- Try incognito/private mode to test

### Styling Issues

- Ensure the entire HTML file is intact
- Check for browser compatibility
- Update to the latest browser version

## Future Enhancements

Potential features for future versions:

- [ ] Quiz categories/topics
- [ ] Difficulty levels
- [ ] Custom quiz creation
- [ ] Export results to PDF
- [ ] Timed quiz mode
- [ ] Question shuffling
- [ ] Image-based questions
- [ ] Leaderboard system

## License

This project is free to use and modify for personal and commercial purposes.

## Contributing

Feel free to fork, modify, and improve this quiz application. Suggestions for improvements:

- Add more question categories
- Implement difficulty levels
- Create admin panel for question management
- Add social sharing features
- Implement user authentication

## Support

For issues or questions:

- Check the troubleshooting section above
- Review the code comments for implementation details
- Test in different browsers to isolate issues

## Credits

Built with vanilla JavaScript - no frameworks or libraries required.

-----

**Version:** 1.0.0  
**Last Updated:** May 18, 2026  
**File Size:** ~10KB  
**Questions:** 10 (Web Development themed)
