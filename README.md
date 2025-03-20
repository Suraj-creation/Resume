# Resume Enhancer

**Resume Enhancer** is an advanced, AI-driven web application designed to transform job seekers' resumes into polished, professional documents optimized for both human recruiters and applicant tracking systems (ATS). Leveraging cutting-edge natural language processing (NLP), machine learning, and an intuitive user interface, this tool guides users through a 10-step process to refine their resumes, ensuring they are competitive, ATS-compatible, and tailored to their career goals. Whether you're a novice job seeker or a seasoned professional, Resume Enhancer empowers you with automation, real-time feedback, and customization to craft a standout resume.

---

## Table of Contents

- [Features](#features)
- [Technologies Used](#technologies-used)
- [Project Workflow](#project-workflow)
- [Installation](#installation)
- [Usage](#usage)
- [Demo Video](#demo-video)
- [Contribution Guidelines](#contribution-guidelines)
- [License](#license)
- [Contact Information](#contact-information)

---

## Features

- **Secure Authentication**: Login/register with email/password, social media integration (Google, LinkedIn), and multi-factor authentication (MFA) for enhanced security.
- **Flexible Upload**: Supports multiple resume formats (PDF, DOCX, RTF, ODT, TXT, HTML) with automatic PDF conversion and file validation (e.g., 10MB limit).
- **Intelligent Extraction**: Parses resumes into structured sections (e.g., Skills, Experience) using NLP and OCR, with color-coded feedback (red for errors, yellow for improvements, orange for weak sections).
- **Dual AI Scoring**: Assesses resumes with two scores (0-100):
  - **GenAI Score**: Evaluates generative AI expertise (e.g., GANs, transformers).
  - **AI Score**: Measures broader AI/ML knowledge (e.g., deep learning, NLP).
- **Tailored Suggestions**: Provides actionable recommendations to improve low-scoring resumes, such as keyword optimization, phrasing enhancements, and quantifiable achievements.
- **Real-Time Editing**: Applies AI suggestions instantly with a live preview, offering drag-and-drop reordering, manual edits, and ATS compatibility checks.
- **Professional Formatting**: Features a library of ATS-friendly templates with customization options (e.g., fonts, colors) and dynamic content fitting.
- **Export Options**: Downloads the final resume as a PDF, with support for DOCX, TXT, and direct uploads to job platforms (e.g., LinkedIn, Indeed).
- **User Empowerment**: Includes version history, collaborative editing, gamification (e.g., badges), and multilingual support for a personalized experience.

---

## Technologies Used

### Backend
- **Python 3.8+**: Core language for processing and logic.
- **Flask**: Lightweight web framework for routing and API development.
- **Supabase**: Cloud-based PostgreSQL database for user data and resume storage.
- **MongoDB**: NoSQL database for flexible document management.
- **SQLAlchemy**: ORM for SQL database interactions.

### AI and NLP
- **Hugging Face Transformers**: Powers text generation, paraphrasing, and scoring (e.g., BERT, T5).
- **spaCy**: Extracts entities and structures resume content.
- **NLTK**: Analyzes keyword density and text quality.
- **KeyBERT**: Identifies critical keywords for optimization.
- **TextBlob**: Enhances sentiment and phrasing in suggestions.
- **Tesseract OCR**: Extracts text from image-based PDFs.

### File Processing
- **PyPDF2**: Handles PDF uploads and metadata extraction.
- **python-docx**: Converts DOCX files to PDF.
- **LibreOffice**: Converts RTF, ODT, and other formats to PDF (via CLI integration).
- **ReportLab**: Generates high-quality PDFs for export.
- **PDFKit**: Converts HTML/CSS designs to PDF.

### Frontend
- **HTML5/CSS3/JavaScript**: Builds a responsive, interactive UI.
- **React**: Dynamic frontend framework for real-time updates and previews.
- **Font Awesome**: Adds icons for visual enhancement.
- **Google Fonts API**: Provides professional, ATS-friendly fonts.

### Security
- **JWT (JSON Web Tokens)**: Secures user authentication.
- **AES-256**: Encrypts resume files during upload/storage.
- **HTTPS**: Ensures secure data transmission.

### External Integrations
- **GitHub API**: Imports project details for tech resumes.
- **LinkedIn API**: Verifies profile data and enhances content.
- **LanguageTool API**: Checks grammar and style.
- **Twilio API**: Sends SMS/email notifications.
- **Unsplash API**: Adds subtle design elements for creative resumes.

---

## Project Workflow

The Resume Enhancer follows a 10-step process, each meticulously designed to refine and optimize your resume:

### 1. Start/Login
- **Purpose**: Initiates a secure, personalized session.
- **Features**: Social media login, MFA, session timeout with auto-save.
- **Tech**: JWT, OAuth, Supabase for user management.

### 2. Resume PDF Upload
- **Purpose**: Captures the raw resume for processing.
- **Features**: Multi-format support, upload feedback (progress bar), file preview, encryption.
- **Tech**: PyPDF2, LibreOffice, AES-256, MongoDB for storage.

### 3. Key Feature Extraction
- **Purpose**: Breaks down the resume into structured sections with visual feedback.
- **Features**: Color-coded highlights (red: errors, yellow: improvements, orange: weak areas), interactive preview, multilingual support.
- **Tech**: spaCy, Tesseract OCR, Hugging Face Transformers.

### 4. AI-Based Scoring
- **Purpose**: Evaluates resume quality and directs the enhancement flow.
- **Features**: Dual scores (GenAI, AI), industry-specific keywords, detailed feedback.
- **Tech**: NLTK, KeyBERT, custom scoring algorithms.

### 5. Suggest Solutions
- **Purpose**: Offers tailored improvements for low-scoring resumes (0-60).
- **Features**: Contextual analysis, quantification prompts, job-specific tailoring.
- **Tech**: Hugging Face Transformers, rule-based suggestion engine.

### 6. Real-Time Updation
- **Purpose**: Applies enhancements instantly with user control.
- **Features**: Live preview, drag-and-drop reordering, ATS compatibility checker, version history.
- **Tech**: React, custom ATS simulator, Supabase sync.

### 7. Enhanced Resume
- **Purpose**: Compiles all improvements into a polished draft.
- **Features**: Keyword optimization, grammar checks, layout adjustments.
- **Tech**: LanguageTool API, ReportLab, spaCy.

### 8. Edit (Optional)
- **Purpose**: Allows manual customization of the AI-enhanced resume.
- **Features**: WYSIWYG editor, inline AI suggestions, template switching, collaboration tools.
- **Tech**: ContentEditable HTML, difflib, React.

### 9. Standard Format
- **Purpose**: Applies a professional, ATS-friendly template.
- **Features**: Template library, real-time preview, content fit management, ATS validation.
- **Tech**: LaTeX, PDFKit, AI-driven template fitting.

### 10. Download PDF Format
- **Purpose**: Delivers the final resume for job applications.
- **Features**: Multi-format export (PDF, DOCX, TXT), cloud sync, email delivery, job platform integration.
- **Tech**: ReportLab, Twilio API, LinkedIn API.

---

## Installation

To set up Resume Enhancer locally for development or testing:

### Prerequisites
- Python 3.8+
- Node.js (for React frontend)
- Git
- MongoDB (local or cloud)
- Supabase account (optional)

### Steps
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/yourusername/resume-enhancer.git
   cd resume-enhancer
