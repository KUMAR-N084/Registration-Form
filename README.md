# Enhanced Registration Form Validation

## Overview
Advanced client-side validation system for a comprehensive registration form with intelligent data quality checks, preventing dummy values, repetitive patterns, and gibberish input.

## Key Features

### 🛡️ Smart Validation Engine
- **Real-time field validation** with instant visual feedback
- **Custom validators** for specialized field requirements
- **Field blocking** - prevents navigation until errors are resolved
- **Debounced form checks** for optimal performance

### 📧 RFC 5322 Compliant Email Validation
- Validates local part (max 64 chars) and domain (max 255 chars)
- Prevents consecutive/leading/trailing dots
- Requires at least one letter in local part and domain labels
- Supports subdomains and special characters (+._-%)
- TLD validation (2-6 letters only)
- Rejects gibberish domains

### 🚫 Dummy Data Detection
Comprehensive blacklist includes:
- Test emails: `test@test.com`, `admin@example.com`, `demo@demo.com`, etc.
- Test usernames: `test`, `admin`, `user`, `demo`, `qwerty`, `password`, etc.
- Invalid phone numbers: `1234567890`, `9999999999`, `1111111111`, etc.

### 🔄 Gibberish & Repetitive Pattern Detection
Intelligent algorithm rejects:
- Keyboard mashing: `jsdkjsdjkvb`, `qwertyasdf`
- Repetitive sequences: `adadadadada`, `asdfasdfasdf`, `1111111111`
- Consonant-heavy gibberish (>75% consonants in 8+ char fields)
- Applies to: names, email, username, mobile, address, postal code, passwords, security answers

### 👤 Enhanced Name Fields
- Accepts single characters: `A`, `J` (initials/single letter names)
- Supports apostrophes: `O'Brien`, `D'Angelo`
- Supports hyphenation: `Jean-Paul`
- Multiple spaces/words: `Mary Ann`
- Prevents leading/trailing spaces and dummy names

### 📱 Mobile Validation
- Exactly 10 digits starting with 6, 7, 8, or 9 (Indian format)
- Blocks dummy/repetitive numbers
- Filters to digits only during input

### 🔐 Password Security
- Minimum 8 characters
- Requires: uppercase, lowercase, digit, special character
- Rejects repetitive patterns
- Confirm password matching

### 📸 Photo Upload Validation
- Supported formats: JPG, JPEG, PNG, SVG
- File size: 1KB - 5MB
- Image dimensions: 100x100px - 5000x5000px
- Real-time preview with error handling

### 🌍 Location Cascading
- Country → State → City auto-population
- Auto-fill from postal code database
- Dependent fields disable until parent selection

### 👶 Age Verification & Parental Consent
- Automatic age calculation from DOB
- Parental consent section for users aged 13-17
- Guardian name, email, phone collection

### ♿ Accessibility Features
- ARIA labels, descriptions, and live regions
- Keyboard navigation support
- Screen reader compatible
- Focus management and visual indicators

## Technical Stack
- **Vanilla JavaScript** - No dependencies
- **HTML5** - Semantic markup
- **CSS3** - Modern styling with animations
- **Font Awesome 6.5** - Icons

## Form Fields
- First Name, Last Name (with enhanced validation)
- Username (with blacklist detection)
- Email (RFC 5322 compliant)
- Mobile Number (Indian format)
- Date of Birth (age verification)
- Postal/Pin Code (with auto-fill)
- Country, State, City (cascading dropdowns)
- Education Level
- Password & Confirm Password
- Gender (radio buttons)
- Address (textarea)
- Security Question & Answer
- Profile Photo Upload
- Terms & Conditions Acceptance
- Guardian Information (conditional for minors)

## Validation Features
| Feature | Status |
|---------|--------|
| No dummy values | ✅ Implemented |
| No repetitive patterns | ✅ Implemented |
| No gibberish input | ✅ Implemented |
| RFC-compliant email | ✅ Implemented |
| Field-level error messages | ✅ Implemented |
| Real-time validation | ✅ Implemented |
| Field blocking on error | ✅ Implemented |
| Accessible form | ✅ Implemented |

## Usage
1. Replace existing `script.js` with enhanced version
2. All validation runs automatically on user input
3. Form submission only enabled when all fields are valid
4. Visual feedback provided for each field (green valid, red invalid)

## Error Messages
- "No gibberish or repetitive patterns allowed"
- "Valid email required"
- "Exactly 10 digits starting with 6, 7, 8, or 9"
- "Letters, spaces, dots, apostrophes. No repeated patterns"
- Field-specific validation messages for each rule

## Browser Support
- Chrome/Edge 90+
- Firefox 88+
- Safari 14+
- Modern mobile browsers

## Notes
- No external validation libraries required
- All validation performed client-side
- Ready for backend integration for duplicate checking
- Easily customizable blacklist and validation rules
  
**#output**

<img width="1115" height="875" alt="Screenshot 2025-12-27 102032" src="https://github.com/user-attachments/assets/a47e87cc-9910-4887-ad2c-5b48eb1180c2" />
<img width="1182" height="872" alt="Screenshot 2025-12-27 102104" src="https://github.com/user-attachments/assets/695afbd0-c21d-4870-9d25-50322978bb6d" />
<img width="1347" height="875" alt="Screenshot 2025-12-27 102118" src="https://github.com/user-attachments/assets/d472d785-fedb-4188-b8fe-cdaf0a49d8f3" />

