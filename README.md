
# 🚀 Smart AI Resume Enhancer

> An intelligent, comprehensive resume analysis and optimization platform powered by AI

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![Streamlit](https://img.shields.io/badge/Streamlit-1.28+-red.svg)](https://streamlit.io)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Build Status](https://img.shields.io/badge/Build-Passing-brightgreen.svg)](https://github.com/Adityaa024/AI-Resume-Enhancer)

## 🎯 Overview

Smart AI Resume Enhancer is a cutting-edge application that leverages artificial intelligence to help professionals create, analyze, and optimize their resumes for maximum impact. Whether you're a job seeker looking to improve your resume or a recruiter seeking to streamline the screening process, this tool provides comprehensive insights and actionable recommendations.

### ✨ Key Features

- **🔍 Intelligent Resume Analysis**: Advanced NLP-powered analysis with ATS compatibility scoring
- **🎨 AI-Powered Resume Builder**: Create professional resumes with multiple customizable templates
- **📊 Interactive Analytics Dashboard**: Comprehensive analytics with visual insights
- **🎯 Job Matching & Search**: Smart job search with role-specific recommendations
- **💼 Skills Gap Analysis**: Identify missing skills and get targeted improvement suggestions
- **📈 Performance Tracking**: Monitor your resume optimization progress over time
- **🤖 AI-Driven Recommendations**: Get personalized suggestions for content improvement
- **📱 Modern Responsive UI**: Clean, intuitive interface built with Streamlit

## 🛠️ Technology Stack

### Frontend & UI
- **Streamlit** - Interactive web application framework
- **HTML/CSS/JavaScript** - Custom styling and enhanced interactivity
- **Plotly** - Interactive data visualizations
- **Streamlit Components** - Enhanced UI elements

### Backend & Processing
- **Python 3.8+** - Core application logic
- **spaCy** - Natural language processing and entity recognition
- **NLTK** - Text processing and analysis
- **scikit-learn** - Machine learning models for text analysis
- **Pandas** - Data manipulation and analysis

### AI & ML Integration
- **Google Generative AI** - Advanced content analysis and suggestions
- **OpenRouter API** - Multi-model AI integration
- **Custom ML Models** - Trained models for resume scoring

### File Processing
- **PyPDF2 & pdfplumber** - PDF parsing and text extraction
- **python-docx** - Word document processing
- **pdf2image & pytesseract** - OCR capabilities for scanned documents
- **reportlab** - PDF generation and formatting

### Database & Storage
- **SQLite3** - Local data storage and management
- **SQLAlchemy** - Database ORM and management

### Automation & Web Scraping
- **Selenium** - Automated web interactions
- **BeautifulSoup** - Web scraping for job portals
- **ChromeDriver** - Browser automation support

## 🚀 Quick Start  

### Prerequisites

- Python 3.8 or higher
- pip (Python package installer)
- Git

### Installation

1. **Clone the repository**
```bash
git clone https://github.com/Adityaa024/AI-Resume-Enhancer.git
cd AI-Resume-Enhancer
```

2. **Create a virtual environment** (recommended)
```bash
# Windows
python -m venv venv
venv\Scripts\activate

# macOS/Linux
python3 -m venv venv
source venv/bin/activate
```

3. **Install dependencies**
```bash
pip install -r requirements.txt
```

4. **Download required NLP models**
```bash
python -m spacy download en_core_web_sm
python -m nltk.downloader punkt stopwords
```

5. **Set up environment variables** (optional)
```bash
# Create .env file for API keys
GOOGLE_API_KEY=your_google_api_key_here
OPENROUTER_API_KEY=your_openrouter_api_key_here
```

6. **Initialize the database**
```bash
python -c "from config.database import init_database; init_database()"
```

7. **Run the application**
```bash
streamlit run app.py
```

The application will be available at `http://localhost:8501`

## 📱 Usage Guide

### 1. Resume Analysis
- Upload your resume in PDF or Word format
- Get instant ATS compatibility scores
- Receive detailed feedback on content, structure, and keywords
- View skills gap analysis for your target role

### 2. Resume Builder
- Choose from multiple professional templates
- Input your information through guided forms
- Get AI-powered content suggestions
- Download your optimized resume as PDF

### 3. Job Search Integration
- Search for relevant job opportunities
- Get role-specific optimization recommendations
- Track application status and feedback

### 4. Analytics Dashboard
- Monitor your resume performance over time
- View detailed analytics on optimization progress
- Access historical data and trends

## 🏗️ Project Structure

```
Smart-AI-Resume-Analyzer/
├── app.py                 # Main Streamlit application
├── requirements.txt       # Python dependencies
├── config/               
│   ├── database.py       # Database configuration
│   ├── job_roles.py      # Job role definitions
│   └── courses.py        # Course recommendations
├── utils/
│   ├── ai_resume_analyzer.py    # AI analysis engine
│   ├── resume_builder.py        # Resume builder utilities
│   ├── resume_analyzer.py       # Core analysis logic
│   └── resume_parser.py         # Resume parsing utilities
├── jobs/
│   ├── job_search.py            # Job search functionality
│   ├── linkedin_scraper.py      # LinkedIn integration
│   └── suggestions.py           # Job recommendations
├── dashboard/
│   ├── dashboard.py             # Analytics dashboard
│   └── components.py            # Dashboard components
├── feedback/
│   ├── feedback.py              # User feedback system
│   └── schema.sql               # Feedback database schema
├── assets/                      # Static assets
├── style/                       # CSS styling
└── poppler/                     # PDF processing tools
```

## 🔧 Configuration

### API Keys Setup

The application supports multiple AI providers. Configure your API keys in a `.env` file:

```env
# Google Generative AI
GOOGLE_API_KEY=your_google_api_key

# OpenRouter API (for multiple models)
OPENROUTER_API_KEY=your_openrouter_api_key
```

### Database Configuration

The application uses SQLite by default. For production deployment, you can configure PostgreSQL or MySQL in `config/database.py`.

### Customization

- **Templates**: Add new resume templates in the `utils/resume_builder.py`
- **Job Roles**: Extend job role definitions in `config/job_roles.py`
- **Styling**: Customize the UI in `style/style.css`

## 🚀 Deployment

### Docker Deployment

```bash
# Build the Docker image
docker build -t smart-resume-ai .

# Run the container
docker run -p 8501:8501 smart-resume-ai
```

### Cloud Deployment

The application is ready for deployment on:
- **Streamlit Cloud** - Direct deployment from GitHub
- **Heroku** - Using the provided `Procfile`
- **AWS/GCP/Azure** - Using Docker containers

For detailed deployment instructions, see [DEPLOYMENT.md](DEPLOYMENT.md).

## 🤝 Contributing

We welcome contributions from the community! Here's how you can help:

1. **Fork the repository**
2. **Create a feature branch**
   ```bash
   git checkout -b feature/amazing-feature
   ```
3. **Make your changes**
4. **Add tests** for new functionality
5. **Commit your changes**
   ```bash
   git commit -m 'Add some amazing feature'
   ```
6. **Push to the branch**
   ```bash
   git push origin feature/amazing-feature
   ```
7. **Open a Pull Request**

### Development Guidelines

- Follow PEP 8 style guidelines
- Add docstrings to all functions and classes
- Include type hints where applicable
- Write unit tests for new features
- Update documentation as needed

## 📊 Features Roadmap

- [ ] **Multi-language Support** - Support for resumes in multiple languages
- [ ] **Advanced AI Models** - Integration with latest language models
- [ ] **Video Resume Analysis** - Analysis of video resumes and interviews
- [ ] **Blockchain Verification** - Resume authenticity verification
- [ ] **Mobile App** - Native mobile application
- [ ] **API Integration** - RESTful API for third-party integrations
- [ ] **Advanced Analytics** - Machine learning insights and predictions

## 🐛 Known Issues & Troubleshooting

### Common Issues

1. **PDF Processing Errors**
   - Ensure Poppler is properly installed
   - Check PDF file permissions and format

2. **Memory Issues with Large Files**
   - Optimize file size before upload
   - Consider breaking large documents into sections

3. **API Rate Limits**
   - Implement proper error handling
   - Use multiple API keys for higher throughput

For more troubleshooting help, check our [Issues](https://github.com/Adityaa024/AI-Resume-Enhancer/issues) page.

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **spaCy** team for excellent NLP capabilities
- **Streamlit** team for the amazing web app framework
- **OpenAI** and **Google** for AI model access
- **Contributors** who help improve this project

## 📞 Support & Contact

- **Issues**: [GitHub Issues](https://github.com/Adityaa024/AI-Resume-Enhancer/issues)
- **Discussions**: [GitHub Discussions](https://github.com/Adityaa024/AI-Resume-Enhancer/discussions)
- **Email**: support@smart-resume-ai.com

## ⭐ Star History

[![Star History Chart](https://api.star-history.com/svg?repos=Adityaa024/AI-Resume-Enhancer&type=Date)](https://star-history.com/#Adityaa024/AI-Resume-Enhancer&Date)

---

<div align="center">
  <p>Made with ❤️ by the Smart Resume AI Team</p>
  <p>
    <a href="#-smart-ai-resume-analyzer">Back to Top</a>
  </p>
</div>
  ```bash
  source venv/bin/activate
  ```

3. **Install dependencies:**

Install the required Python packages:

   ```bash
   pip install -r requirements.txt
   ```

4. **Download the spaCy model:**

Ensure that the necessary NLP model is installed:

   ```bash
   python -m spacy download en_core_web_sm
   ```
   
``Congratulations 🥳😱 your set-up 👆 and installation is finished 🥳😱``


5. **Configure Environment Variables (Mandatory for AI-Analyzer Functionality):**

To enable access to the **Gemini API** used by the AI Resume Analyzer, you need to set up environment variables securely.

#### ✅ Step-by-Step:

1. **Create a `.env` file** inside the `utils/` directory.
2. **Paste your Google Gemini API key** in the following format:

#### 📄 Example content for `utils/.env`:
```env
GOOGLE_API_KEY=your_google_gemini_api_key
```

#### <img src="https://assets.codepen.io/1468070/Google+G+Icon.png" alt="Google LOGO" width="1.6%" /> Get your Gemini API Key:
Visit  **[Google AI Studio – Gemini API Access](https://aistudio.google.com/app/apikey)** 👉 Grab and use your **own API key** — Since Mine One Have Usage Limits.


6. **Run the application:**

Start the application using Streamlit:

   ```bash
   streamlit run app.py
   ```

<details>
  <summary>📁 Folder Structure After Adding <code>.env</code></summary>

> 🔐 **Important:**  
> - **Do not commit your `.env` file** to version control (e.g., GitHub). It should be listed in `.gitignore`.
> - If you're collaborating, you can provide a safe `.env.example` file with dummy data.

  <div align="center">  
    <table>
      <tr>
        <td align="center"><b>🗂️ Folder Structure Preview 1</b></td>
        <td align="center"><b>🗂️ Folder Structure Preview 2</b></td>
      </tr>
      <tr>
        <td>
          <img src="https://github.com/user-attachments/assets/a6636ec0-f1e6-45ed-90f5-583ecbf7f67f" alt="Folder Structure Preview 1" height="350px" width="600px">
        </td>
        <td>
          <img src="https://github.com/user-attachments/assets/10fea5d7-5b9f-491e-871f-75a9ab716ebb" alt="Folder Structure Preview 2" height="355px" width="600px">
        </td>
      </tr>
    </table>
  </div>
  

</details>

## Admin Login Credentials

### 🔹 New Login Credentials:
   - **Username:**
```python3
admin@example.com
```
   - **Password:**
```python3
admin123
```

### 🔹 Admin Panel Access:
   - The **Admin Section** will be visible **only after login**, right below the **Dashboard** section.

<!--### Deploy to Streamlit Cloud

1. Push your code to GitHub
2. Sign up for [Streamlit Cloud](https://streamlit.io/cloud)
3. Create a new app and connect it to your GitHub repository
4. Add your API keys as secrets in the Streamlit Cloud dashboard
5. Deploy the app

### Deploy with Docker

1. Build the Docker image:
   ```bash
   docker build -t smart-resume-analyzer .
   ```

2. Run the container:
   ```bash
   docker run -p 8501:8501 -e GOOGLE_API_KEY=your_key smart-resume-analyzer
   ```

## Project Structure

```
Smart-AI-Resume-Analyzer/
├── app.py                  # Main application file
├── config/                 # Configuration files
│   ├── courses.py          # Course recommendations
│   ├── database.py         # Database operations
│   └── job_roles.py        # Job role definitions
├── dashboard/              # Dashboard components
├── feedback/               # Feedback system
├── jobs/                   # Job search functionality
├── static/                 # Static assets
│   ├── css/                # CSS files
│   └── images/             # Image files
├── style/                  # Style definitions
├── templates/              # Resume templates
├── ui_components/          # UI components
├── utils/                  # Utility functions
│   ├── ai_resume_analyzer.py  # AI analysis logic
│   ├── resume_analyzer.py     # Standard analysis logic
│   └── resume_builder.py      # Resume builder logic
├── .env                    # Environment variables (not in git)
├── .gitignore              # Git ignore file
├── Dockerfile              # Docker configuration
├── LICENSE                 # License file
├── README.md               # This file
└── requirements.txt        # Python dependencies
```

## Troubleshooting

### Common Issues

1. **PDF Extraction Fails**: Ensure Tesseract OCR is properly installed and in your PATH
2. **API Key Errors**: Verify your API keys in the `.env` file
3. **Missing Dependencies**: Run `pip install -r requirements.txt` again

### Getting Help

If you encounter any issues, please [open an issue](https://github.com/yourusername/Smart-AI-Resume-Analyzer/issues) on GitHub.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request
-->

## Known Bug 🚨 Autofill Glitch in Resume Builder!  

### What's Happening? 🤔  
If you're using the **Browser's (e.g., Chrome, Edge, etc.) Autofill** feature to quickly fill out your **Name**, **Email**, and **Phone** details in our **Smart AI Resume Analyzer**, you might encounter this error in generating Resume:  
**"⚠️ Please enter your email address."**  

Even though the email field appears to be filled, this is a small bug in the **Resume Builder Feature** where our system doesn't always recognize inputs from autofill.

### Quick Fix 🛠️  
Don't worry—it's a simple fix!  
1. **Edit the email(or Any) field manually:**  
   - Remove one character or number.  
   - Type it back in.  
2. Voilà! The error will disappear, and you can generate your resume smoothly.  
> _(“Voilà” means "there you have it!" or "problem solved!")_

### Why Does This Happen? 🌐  
This is a **known issue with the resume builder feature**, where the autofill behavior of browsers (e.g., Chrome, Edge, etc.) doesn't trigger the necessary validation for some input fields. By manually editing the email, the system recognizes it correctly.  

We're actively working on a permanent fix to ensure your experience is seamless. Thank you for your understanding and support! 🙏  


## 🎯 **Why Choose Smart Resume AI?**  

✨ **Tailored for You**  
Your resume is optimized for the job you're aiming for, using role-specific insights.  

🖼️ **Stunning Templates**  
Choose from polished and modern templates that stand out at first glance.  

⚡ **Time-Saving Automation**  
AI does the heavy lifting, helping you create a winning resume in minutes.  

📈 **Better Chances, Every Time**  
Get actionable feedback and align your resume to job descriptions effortlessly.  


## <img src="https://github.com/user-attachments/assets/1fd5ec3c-a43f-4df6-b9ec-31102a6b6564" width="30px"> **Contributing**  

Join the mission! Here's how:  
1. Fork the repository.  
2. Create a new branch for your feature: `git checkout -b feature-name`.  
3. Push changes and submit a Pull Request.  

##  <img src="https://github.com/user-attachments/assets/5b3cb883-6652-4525-a352-b4b9a3501e07" width = 35px height = 35px> **Why Users Love Smart Resume AI**  

- **Saves Time:** Create a stunning resume in minutes.  
- **Increases Job Opportunities:** Tailor your resume to any role.  
- **Professional Output:** Choose from modern and polished designs.  
- **Boosts Confidence:** Optimized, recruiter-ready resumes.  

## <img src="https://github.com/user-attachments/assets/e5ac1371-6ac4-48b6-b95c-5ef9afaf1353" width="30"> **Features That Set Us Apart**  

| **Feature**                   | **Description**                                                                                 |  
|--------------------------------|-------------------------------------------------------------------------------------------------|  
| 🔍 **Resume Analysis**         | Get an ATS score, identify keyword gaps, and find skills to add for role alignment.             |  
| ✨ **Customizable Templates**  | Choose from **4 sleek designs**: Modern, Minimal, Professional, Creative.                       |  
| 📈 **AI-Driven Insights**      | Receive smart suggestions for optimizing content, formatting, and keywords.                    |  
| 🎯 **Role-specific Guidance**  | Tailored recommendations for matching job descriptions and standing out in applications.        |  

## 🎥 **Quick Glance**  

<div align="center">  
<table>  
<tr>  
<td align="center"><b>
   
   [🏠 HOME]
   </b></td>  
<td align="center"><b>
   
   [🔍 RESUME ANALYZER(Below Example Analysis of Backend Deeveloper)]
</b></td>  
</tr>  
<tr>  
<td><img src="https://github.com/user-attachments/assets/2dc1b44d-7eb6-4371-81f9-3a140f83064c" alt="🏠 HOME" width="500px"></td>  
<td><img src="https://github.com/user-attachments/assets/b9f4c7b0-fbd6-40c4-9d8b-231d9fdd91a7" alt="🔍 RESUME ANALYZER" width="500px"></td>  
</tr>  
<tr>  
<td align="center"><b>
   
   [🔍 RESUME ANALYZER(Score And Recommendations)]
   </b></td>  
<td align="center"><b>
   
   [🔍 RESUME ANALYZER(According To Roles Recommendations)]
   </b></td>  
</tr>  
<tr>  
<td><img src="https://github.com/user-attachments/assets/02b6d379-a04f-421e-9377-1bb077324f17" alt="🔍 RESUME ANALYZER(Score And Recommendations Based on Role Selected)" width="500px"></td>  
<td><img src="https://github.com/user-attachments/assets/830e738e-a76b-4818-b426-d98189d8c441" alt="🔍 RESUME ANALYZER(Score And Recommendations Based on Role Selected)" width="500px"></td>  
</tr>  

<tr>  
<td align="center"><b>
   
   [🔍 RESUME ANALYZER(According To Roles Course Recommendations)]
   </b></td>  
<td align="center"><b>
   
   [🔍 RESUME ANALYZER(Videos Recommendations)]
   </b></td>  
</tr>  
<tr>  
<td><img src="https://github.com/user-attachments/assets/fcfb02f2-2831-4f26-a251-8c67266afca8" alt="🔍 RESUME ANALYZER" width="500px"></td>  
<td><img src="https://github.com/user-attachments/assets/90704043-a559-42fb-bcf1-330ebfedee2b" alt="🔍 RESUME ANALYZER" width="500px"></td>  
</tr> 
<tr>  
<td align="center"><b>
   
   
   [🔍 AI Resume Analysis (Custom Job Description)]
   </b></td>  
<td align="center"><b>  
   
   [📊 AI Resume Score & Statistics]
</b></td>  
</tr>  

<tr>  
<td><img src="https://github.com/user-attachments/assets/2105d65a-f01c-4af2-995c-fa29854a4fa1" alt="🔍 AI Resume Analysis with Custom Job Description" width="500px"></td>  
<td><img src="https://github.com/user-attachments/assets/98f3d612-a167-4fbd-a1e2-a0a122d101a6" alt="📊 AI Resume Score & Statistics" width="500px"></td>  
</tr>  

<tr>  
<td align="center"><b>  
   
   [📄 AI-Generated PDF Resume Report]
   </b></td>  
<td align="center"><b>  
   
   [📊 AI Resume Analysis Insights]
   </b></td>  
</tr>  

<tr>  
<td><img src="https://github.com/user-attachments/assets/e74aa01f-36e3-489a-8873-1807389007de" alt="📄 AI-Generated PDF Resume Report" width="500px"></td>  
<td><img src="https://github.com/user-attachments/assets/9c5fbaf9-bb32-468c-b709-8e795d3f1796" alt="📊 AI Resume Analysis Insights" width="500px"></td>  
</tr>  

<tr>  
<td align="center"><b>  
   
   [🔗 LinkedIn Job Scraper (Search Results)]
   </b></td>  
<td align="center"><b>  
   
   [🏢 LinkedIn Scraper (Job Listings UI)]
   </b></td>  
</tr>  

<tr>  
<td><img src="https://github.com/user-attachments/assets/1fedb318-03d9-4cd6-8b40-20714cb53b48" alt="🔗 LinkedIn Job Scraper (Search Results)" width="500px"></td>  
<td><img src="https://github.com/user-attachments/assets/46081404-8cad-4d72-b921-e98103b9918e" alt="🏢 LinkedIn Scraper (Job Listings UI)" width="500px"></td>  
</tr>  

</table>  
</div>  

> Note: **Time Taking For scraping so have Patience**

## 🎨 **Interactive Resume Templates**  

| ![Modern Template](https://github.com/user-attachments/assets/63a7c783-9903-4e45-bdc7-3bfb41f2606b) | ![Minimal Template](https://github.com/user-attachments/assets/ea1ade65-a726-4c67-a19c-2b29d8ab748e) |  
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------|  
| **Modern Template** - Polished & stylish                                  | **Minimal Template** - Clean & elegant                                     |  

| ![Professional Template](https://github.com/user-attachments/assets/003532ae-99ec-41b7-a258-05bf3f97a4cc) | ![Creative Template](https://github.com/user-attachments/assets/0fc2aa14-e24b-473d-964e-2900e49631f1) |  
|-------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|  
| **Professional Template** - Industry-standard                                     | **Creative Template** - Unique & visually appealing                          |  


## 📄 **License**  

This project is licensed under the [MIT License](https://github.com/Adityaa024/AI-Resume-Enhancer/blob/main/LICENSE).  


## 🌟 **GitHub Repo**  

Explore the code, contribute, or drop a <img src="https://github.com/user-attachments/assets/35f6838c-52f5-4e48-8a98-c5203f8c57e3" style="width:20px; color: #FFD700" alt="Star GIF"> : [Smart Resume AI Repository](https://github.com/your-username/resume-analyzer-ai)  

## 🛡️ Maintainer  

> **_This repository is maintained by Aditya Raj(https://github.com/Adityaa024)._**  
> Have suggestions? Feel free to reach out to [me via email](mailto:adityaraj3458@gmail.com). 📧


## 📰 News  
**Practice, practice, practice!** Keep working hard, and it will all fall into place. No shortcuts in this Field! 🛠️  
> Stay curious and keep learning. 🚀

                                 |

**Thank you for your support! Every bit helps keep this repository going.** 🌈✨
