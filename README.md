# Poli Gigi Registration Form

A simple web application that recreates a dental clinic registration form with conditional logic and step-by-step user flow.

## 📋 Overview

This is a prototype web application that demonstrates how to convert a Google Form into an interactive HTML form with conditional branching. The form guides patients through a series of questions to determine the appropriate dental clinic department for their needs.

## 🚀 Features

- **Single HTML File**: Everything is contained in one HTML file with embedded CSS and JavaScript
- **Conditional Logic**: Questions are displayed based on previous answers
- **Step-by-Step Flow**: Users see one question at a time for better user experience
- **Responsive Design**: Works on desktop and mobile devices
- **No Backend Required**: Pure frontend implementation
- **Clean UI**: Google Forms-inspired design

## 🏥 Form Flow

The form follows this decision tree:

1. **Patient Type**
   - **Pedo** → Kiara - Poli Gigi dan Mulut
   - **Dewasa** → Continue to next question

2. **Previous Visit** (for Dewasa)
   - **Belum** → ORAL DIAGNOSTIK
   - **Sudah** → Continue to next question

3. **Time Since Last Visit**
   - **Lebih dari satu tahun** → ORAL DIAGNOSTIK
   - **Kurang dari satu tahun** → Show treatment options

4. **Treatment Options**
   - Tambal gigi dan perawatan saraf gigi → **KONSERVASI**
   - Cabut gigi → **BEDAH MULUT**
   - Gigi palsu → **PROSTHODONTI**
   - Sariawan, sialometri, etc. → **PENYAKIT MULUT**
   - Keluhan gusi → **PERIODONTI**
   - Kawat gigi (non BPJS) → **ORTHODONTI**

## 🛠️ Technologies Used

- **HTML5**: Semantic structure
- **CSS3**: Modern styling with flexbox and transitions
- **Vanilla JavaScript**: No external dependencies
- **Google Fonts**: Roboto for typography

## 📁 File Structure

```
poli-gigi-registration/
├── README.md
└── pendaftaran-poli-gigi.html
```

## 🚀 Getting Started

### Prerequisites
- Any modern web browser (Chrome, Firefox, Safari, Edge)

### Installation
1. Clone or download this repository
2. Open `pendaftaran-poli-gigi.html` in your web browser
3. The form is ready to use

### Local Development (Optional)
If you want to run this locally with a simple HTTP server:

```bash
# Using Python 3
python -m http.server 8000

# Using Node.js
npx serve .

# Using PHP
php -S localhost:8000
```

Then open `http://localhost:8000/pendaftaran-poli-gigi.html` in your browser.

## 🎨 Customization

### Changing Questions
Edit the HTML sections with IDs like `question1`, `question2`, etc.

### Modifying Logic
Update the JavaScript functions in the `<script>` tag:
- `showNextQuestion()` - Handles patient type branching
- `handlePreviousVisit()` - Handles visit history branching  
- `handleTimeSinceVisit()` - Handles time-based branching
- `handleTreatmentType()` - Handles treatment selection

### Styling
Modify the CSS in the `<style>` tag to customize colors, fonts, and layout.

## 🔧 Configuration

No configuration required. The form works out of the box without any external dependencies or API calls.

## 📱 Browser Support

- Chrome 60+
- Firefox 55+
- Safari 12+
- Edge 79+

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📞 Support

This is a prototype application. For questions or suggestions:
- Open an Issue in this repository
- Contact the project maintainer

## 🌟 Acknowledgments

- Inspired by Google Forms' user experience
- Design follows Material Design principles
- Built as a demonstration of frontend capabilities

---

**Note**: This is a demonstration project. In a production environment, you would want to add:
- Form validation
- Database integration
- Error handling
- Accessibility features
- Internationalization
- Analytics tracking