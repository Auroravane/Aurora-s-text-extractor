# 🌌 Aurora Text Extractor

> *Transform handwritten notes and images into digital text with cinematic precision*

A professional, AI-powered OCR (Optical Character Recognition) web application that converts images containing text into editable digital format. Built with cutting-edge design aesthetics and advanced functionality for seamless text extraction.

## ✨ Features

### 🎯 **Core Functionality**
- **Advanced OCR Technology**: Powered by Tesseract.js for superior text recognition accuracy
- **Multi-Language Support**: 12+ languages including English, Spanish, French, German, Italian, Portuguese, Russian, Japanese, Korean, Chinese, Hindi, and Arabic
- **Batch Processing**: Upload and process multiple images simultaneously
- **Real-time Preview**: See all selected images in an organized grid layout
- **Smart Text Processing**: Auto-correction and intelligent formatting options

### 🎨 **Professional Design**
- **Aurora Aesthetic**: Cinematic dark theme with noir-blue gradients and film grain texture
- **Responsive Design**: Optimized for desktop, tablet, and mobile devices
- **Interactive Elements**: Smooth animations, hover effects, and visual feedback
- **Typography System**: Professional font hierarchy using Playfair Display, Inter, and Dancing Script
- **Glassmorphism UI**: Modern backdrop blur effects with sophisticated color palette

### 📁 **File Management**
- **Individual Image Removal**: Remove specific images from selection with dedicated buttons
- **Bulk Operations**: Remove all images or clear entire workspace
- **File Information**: Display filename and file size for each uploaded image
- **Drag & Drop**: Intuitive drag-and-drop interface with visual feedback
- **Multiple Formats**: Support for JPG, PNG, PDF, WebP (up to 10MB per file)

### 📤 **Export Options**
- **Copy to Clipboard**: One-click text copying with visual confirmation
- **TXT Download**: Plain text file with timestamp
- **PDF Generation**: Professional PDF with title, timestamp, and formatted content
- **DOCX Export**: Microsoft Word document with proper styling and metadata
- **Real-time Editing**: Edit extracted text before downloading

### 🔒 **Privacy & Security**
- **Local Processing**: All OCR processing happens in your browser
- **No Server Upload**: Images never leave your device
- **No Data Storage**: No personal information collected or stored
- **Offline Capable**: Works without internet connection after initial load

## 🚀 Quick Start

### **Option 1: Direct Use**
1. Download all files (`index.html`, `script.js`, `styles.css`)
2. Open `index.html` in any modern web browser
3. Start uploading images and extracting text immediately

### **Option 2: Local Development**
```bash
# Clone or download the project
git clone <repository-url>
cd aurora-text-extractor

# Serve locally (optional, for development)
npx http-server
# or
python -m http.server 8000
```

### **Option 3: Deploy to Web**
Upload all files to any web hosting service:
- GitHub Pages
- Netlify
- Vercel
- Traditional web hosting

## 📖 Usage Guide

### **Basic Workflow**
1. **Upload Images**: Click the upload area or drag & drop images
2. **Select Language**: Choose the primary language of your text
3. **Configure Options**: Enable auto-correction and smart formatting as needed
4. **Process Images**: Click "✨ Extract Text" to begin OCR processing
5. **Edit & Export**: Review the extracted text and download in your preferred format

### **Advanced Features**

#### **Multi-Language Processing**
- Click any language flag to switch OCR language
- Supported languages include major world languages with flag indicators
- Automatic language detection works best with clear, high-contrast text

#### **Batch Processing**
- Select multiple images at once for bulk processing
- Each image appears in its own preview card
- Process all images with a single click
- Text from multiple images is automatically combined with separators

#### **Quality Controls**
- **Auto-Correct**: Fixes common OCR errors like spacing and punctuation
- **Smart Formatting**: Preserves document structure and removes excess whitespace
- **Manual Editing**: Edit extracted text directly in the output area before downloading

#### **Individual Image Management**
- **Remove Specific Images**: Click the 🗑️ button on any image card
- **Batch Removal**: Use "Remove All Images" to clear image selection
- **File Information**: View filename and size for each uploaded image
- **Visual Feedback**: Real-time updates showing remaining file count

### **Keyboard Shortcuts**
- `Ctrl/Cmd + U`: Quick upload shortcut
- `Ctrl/Cmd + Enter`: Start processing (when images are loaded)
- `Ctrl/Cmd + Shift + C`: Copy extracted text to clipboard

## 🛠️ Technical Details

### **Technology Stack**
- **Frontend**: Pure HTML5, CSS3, JavaScript ES6+
- **OCR Engine**: Tesseract.js v5
- **PDF Generation**: jsPDF v2.5.1
- **DOCX Export**: docx.js v8.5.0
- **Fonts**: Google Fonts (Inter, Playfair Display, Dancing Script)

### **Browser Compatibility**
- ✅ Chrome 90+
- ✅ Firefox 88+
- ✅ Safari 14+
- ✅ Edge 90+
- ✅ Mobile browsers (iOS Safari, Chrome Mobile)

### **Performance Specifications**
- **File Size Limit**: 10MB per image
- **Supported Formats**: JPG, PNG, PDF, WebP
- **Processing Speed**: ~2-5 seconds per image (varies by image complexity)
- **Memory Usage**: Optimized for efficient processing with automatic cleanup

### **Architecture**
```
Aurora Text Extractor/
├── index.html          # Main HTML structure
├── embedded CSS        # Aurora styling system
├── embedded JavaScript # Core application logic
└── External Libraries  # CDN-loaded dependencies
    ├── Tesseract.js    # OCR engine
    ├── jsPDF           # PDF generation
    └── docx.js         # Word document export
```

## 🎨 Design Philosophy

### **Aurora Style Aesthetic**
The application embodies the "Aurora Style" design philosophy:

- **"Poet in Shadows"**: Deep noir-blue backgrounds creating cinematic atmosphere
- **Whispering Transitions**: Smooth, staggered animations that feel like held breath
- **Golden Ratio Proportions**: Mathematical precision in layout and spacing
- **Cinematic Texture**: Film grain and subtle effects for authentic feel
- **Breathing Space**: Strategic negative space for visual comfort

### **Color Palette**
- **Primary**: Noir Blue (#0A0F1C) with gradient overlays
- **Accents**: Cinematic Teal (#00A3E0), Twilight Purple (#6B4E71)
- **Text**: Candle White (#F2E9E4), Haze Pink (#C7BFD7)
- **Interactive**: Deep Crimson (#A30000) for destructive actions

## 🔧 Customization

### **Adding New Languages**
```html
<div class="language-option" data-lang="new_lang_code">🏳️ XX</div>
```

### **Modifying OCR Settings**
```javascript
// In the extractTextFromFile method
const worker = await Tesseract.createWorker(this.currentLanguage, 1, {
    logger: (m) => this.handleOCRProgress(m),
    // Add custom Tesseract options here
});
```

### **Styling Customization**
All design tokens are defined in CSS custom properties for easy customization:
```css
:root {
    --accent-teal: #00A3E0;     /* Change primary accent color */
    --transition-fast: 0.3s;    /* Adjust animation speed */
    /* ... modify other variables as needed */
}
```

## 📱 Mobile Optimization

### **Responsive Features**
- **Touch-Friendly**: Large tap targets and swipe gestures
- **Mobile Camera**: Direct camera integration for capturing documents
- **Adaptive Layout**: Grid system automatically adjusts to screen size
- **Performance**: Optimized for mobile processors and memory constraints

### **Mobile-Specific Enhancements**
- Larger upload area for easier touch interaction
- Simplified navigation for smaller screens
- Optimized image compression for faster processing
- Battery-conscious processing with efficient algorithms

## 🔍 Troubleshooting

### **Common Issues**

#### **OCR Accuracy Problems**
- **Solution**: Ensure high contrast between text and background
- **Tip**: Use good lighting when photographing documents
- **Best Practice**: Select the correct language for your text

#### **Large File Processing**
- **Issue**: Slow processing on large images
- **Solution**: Resize images to reasonable dimensions (max 2048px width)
- **Tip**: Use JPEG format for photographs, PNG for screenshots

#### **Mobile Performance**
- **Issue**: Slow processing on older mobile devices
- **Solution**: Process one image at a time on slower devices
- **Tip**: Close other browser tabs to free up memory

#### **Download Issues**
- **Problem**: Downloads not working
- **Check**: Ensure text has been extracted first
- **Solution**: Try a different browser if issues persist

### **Browser-Specific Notes**
- **Safari**: May require user interaction before downloading files
- **Mobile Browsers**: Some features may require full-screen mode
- **Firefox**: Excellent performance with all features
- **Chrome**: Recommended browser for optimal experience

## 📊 Performance Tips

### **For Best Results**
1. **Image Quality**: Use high-resolution, well-lit images
2. **File Format**: JPEG for photos, PNG for screenshots
3. **File Size**: Keep images under 5MB for faster processing
4. **Text Clarity**: Ensure text is clearly visible and not blurry
5. **Background**: Plain backgrounds work better than complex patterns

### **Optimization Guidelines**
- Process images in smaller batches for faster results
- Use appropriate language settings for better accuracy
- Enable auto-correction for handwritten text
- Edit extracted text before downloading for best quality

## 🤝 Contributing

### **How to Contribute**
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### **Areas for Contribution**
- Additional language support
- OCR accuracy improvements
- New export formats
- Performance optimizations
- Accessibility enhancements
- Mobile-specific features

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **Tesseract.js** - Powerful OCR engine
- **jsPDF** - Client-side PDF generation
- **docx.js** - Word document creation
- **Google Fonts** - Beautiful typography
- **Aurora Style** - Design philosophy and aesthetic framework

## 📞 Support

### **Getting Help**
- Check the troubleshooting section above
- Review browser compatibility requirements
- Ensure all external libraries are loading properly

### **Reporting Issues**
When reporting bugs, please include:
- Browser version and operating system
- Image types and sizes being processed
- Error messages (if any)
- Steps to reproduce the issue

## 🔮 Future Roadmap

### **Planned Features**
- [ ] Cloud storage integration (Google Drive, Dropbox)
- [ ] Advanced text formatting options
- [ ] OCR confidence scoring
- [ ] Table detection and extraction
- [ ] Handwriting style analysis
- [ ] API endpoint for developers
- [ ] Dark/light theme toggle
- [ ] Custom language model training

### **Version History**
- **v1.0.0** - Initial release with Aurora styling and core OCR functionality
- **v1.1.0** - Added individual image removal and enhanced batch processing
- **v1.2.0** - Planned: Advanced formatting and cloud integration

---

**Built with ❤️ using Aurora Design Philosophy**  
*Where technology meets artistry, and function dances with form*
