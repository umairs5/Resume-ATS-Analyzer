# 🎯 ATS Resume Analyzer

An AI-powered resume analysis and optimization tool that helps job seekers improve their resumes for Applicant Tracking Systems (ATS). Built with Gradio and powered by Groq's LLaMA 3.1 model, this comprehensive tool provides resume analysis, content rephrasing, cover letter generation, and interview question preparation.

## ✨ Features

### 📊 Resume Analyzer
- **ATS-Optimized Analysis**: Comprehensive resume evaluation against job descriptions
- **Match Percentage**: Get exact match scores for job requirements
- **Missing Keywords Detection**: Identify crucial keywords you're missing
- **Improvement Recommendations**: Actionable suggestions with examples
- **General Analysis**: Standalone resume evaluation without job descriptions

### ✏️ Content Rephraser
- **ATS Optimization**: Rephrase content to pass ATS screening
- **Quantifiable Measures**: Add measurable achievements to your content
- **Professional Language**: Transform casual descriptions into professional statements

### 📝 Cover Letter Generator
- **Tailored Content**: Generate personalized cover letters based on your resume and job description
- **Professional Format**: 250-300 word optimized cover letters
- **Company-Specific**: Customized for each role and organization

### 🎤 Interview Questions Generator
- **Role-Specific Questions**: Generate probable interview questions for any job
- **Mixed Question Types**: Technical, behavioral, and cultural fit questions
- **Interview Preparation**: Comprehensive question sets to prepare effectively

## 🚀 Getting Started

### Prerequisites

- Python 3.11+
- Groq API Key (sign up at [groq.com](https://groq.com))

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/umairs5/Resume-ATS-Analyzer.git
   cd ats-resume-analyzer
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Set up environment variables**
   
   Create a `.env` file in the root directory:
   ```env
   GROQ_API_KEY=your_groq_api_key_here
   ```

4. **Run the application**
   ```bash
   python main.py
   ```

5. **Open your browser**
   
   Navigate to `http://localhost:7860`

## 📦 Dependencies

Create a `requirements.txt` file with:

```txt
gradio
groq
PyPDF2
python-docx
python-dotenv
```

## 🎯 How to Use

### Resume Analysis

1. **Upload Your Resume**
   - Supports PDF and DOCX formats
   - Text is automatically extracted and displayed

2. **Choose Analysis Type**
   - **With Job Description**: Check the box and paste the job description for targeted analysis
   - **General Analysis**: Uncheck the box for overall resume evaluation

3. **Get Results**
   - Match percentage and missing keywords
   - Detailed improvement recommendations
   - ATS optimization suggestions

### Content Rephrasing

1. **Enter Text**: Paste any resume content you want to improve
2. **Click Rephrase**: Get ATS-optimized version with better impact
3. **Copy Results**: Use the improved content in your resume

### Cover Letter Generation

1. **Prerequisite**: First analyze your resume with a job description
2. **Generate**: Click "Generate Cover Letter" to create a tailored letter
3. **Review**: Edit and customize the generated content as needed

### Interview Questions

1. **Enter Job Description**: Paste the job posting details
2. **Generate Questions**: Get 10 probable interview questions
3. **Prepare**: Use these questions to practice and prepare

## ⚙️ Customization

### Model Parameters

- **Temperature** (0.0-1.0): Controls response creativity
  - Lower values = more focused responses
  - Higher values = more creative responses

- **Max Tokens** (50-1024): Controls response length
  - Adjust based on desired output length

### Supported File Formats

- **PDF**: Resumes in PDF format
- **DOCX**: Microsoft Word documents

## 🎨 Interface Features

- **Modern UI**: Clean, professional design with dark theme
- **Tabbed Interface**: Organized functionality across multiple tabs
- **Real-time Processing**: Instant text extraction from uploaded files
- **Responsive Design**: Works on desktop and mobile devices
- **Parameter Controls**: Adjustable AI model settings

## 🔧 Technical Details

### Architecture

```
User Input → File Processing → Text Extraction → Groq LLM → AI Analysis → Results Display
```

### Key Components

- **File Processing**: PyPDF2 and python-docx for document parsing
- **AI Processing**: Groq's LLaMA 3.1-8B-Instant model
- **UI Framework**: Gradio for web interface
- **Environment Management**: python-dotenv for configuration

### Analysis Criteria

The tool evaluates resumes based on:

- **Impact**: Quantification, action verbs, responsibilities
- **Brevity**: Length optimization, bullet points, conciseness
- **Style**: Professional language, consistency, active voice
- **Sections**: Proper structure, relevant sections, formatting
- **ATS Compatibility**: Keyword matching, formatting standards

## 🚦 Usage Examples

### Resume Analysis Output
```
Match Percentage: 75%
Missing Keywords: Python, Machine Learning, AWS, Agile
Recommendations:
1. Add quantifiable achievements (e.g., "Increased efficiency by 30%")
2. Include relevant technical skills from job description
3. Use action verbs at the beginning of bullet points
4. Ensure consistent formatting throughout
```

### Rephrased Content Example
```
Original: "Worked on various projects"
Rephrased: "Led 5+ cross-functional projects, delivering solutions that improved operational efficiency by 25%"
```

## 🛠️ Troubleshooting

### Common Issues

1. **"No GROQ_API_KEY found"**
   - Ensure your `.env` file exists and contains the API key
   - Check for typos in the environment variable name

2. **File Upload Issues**
   - Ensure files are in PDF or DOCX format
   - Check file size (large files may take longer to process)

3. **Empty Analysis Results**
   - Verify the resume contains readable text
   - Ensure job description is provided when required

4. **API Rate Limits**
   - If you hit rate limits, wait a moment before trying again
   - Consider upgrading your Groq API plan for higher limits

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Development Setup

```bash
# Clone your fork
git clone https://github.com/yourusername/ats-resume-analyzer.git
cd ats-resume-analyzer

# Create virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Set up pre-commit hooks (optional)
pip install pre-commit
pre-commit install
```

## 📄 File Structure

```
ats-resume-analyzer/
├── main.py              # Main application file
├── requirements.txt     # Python dependencies
├── .env                 # Environment variables (create this)
├── .gitignore          # Git ignore file
└── README.md           # This file
```

## 🔒 Privacy & Security

- **Local Processing**: Files are processed locally and not stored permanently
- **API Security**: Only text content is sent to Groq's API for analysis
- **No Data Retention**: The application doesn't store your resume or personal data
- **Environment Variables**: Sensitive API keys are stored securely in `.env` file

## 📈 Performance Tips

1. **File Size**: Keep resume files under 10MB for faster processing
2. **Internet Connection**: Stable connection required for AI analysis
3. **Browser**: Use modern browsers for best performance
4. **Content Length**: Longer job descriptions may take more time to process

## 🙏 Acknowledgments

- [Groq](https://groq.com/) for providing fast LLM inference
- [Gradio](https://gradio.app/) for the excellent UI framework
- [PyPDF2](https://pypdf2.readthedocs.io/) for PDF processing capabilities
- [python-docx](https://python-docx.readthedocs.io/) for Word document processing

## 🔮 Future Enhancements

- [ ] Multiple resume format support (TXT, RTF)
- [ ] Batch processing for multiple resumes
- [ ] Resume template suggestions
- [ ] Industry-specific analysis
- [ ] Integration with job boards
- [ ] Resume scoring dashboard
- [ ] Export analysis reports

---

⭐ **If this tool helps you land your dream job, please star the repository!**

**Made with ❤️ for job seekers everywhere**
