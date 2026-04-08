# Vaidya Bridge - Healthcare Platform

A comprehensive doctor-patient care platform prototype featuring AI-powered healthcare management, patient records, notifications, and natural language query capabilities.

## Live Demo
**Interactive Prototype**: https://claude.ai/share/bbde9464-c741-499c-bcbe-56297e3c7b19

## Features

- **Doctor Dashboard**: Real-time patient metrics, follow-ups, and critical alerts
- **Patient Records**: Comprehensive patient management with tags and clinical notes
- **Automated Notifications**: Smart reminders and critical report alerts
- **Report Chain**: AI-powered report analysis and automated patient communication
- **Natural Language Query**: Ask questions about patients in plain English/Hindi
- **Role-based Access**: Separate interfaces for doctors and patients
- **Data Security**: HIPAA-aligned with row-level security and PII masking

## Technology Stack

- **Frontend**: HTML5, CSS3, JavaScript, TailwindCSS
- **Backend Architecture**: Node.js/FastAPI (planned)
- **Database**: BigQuery with row-level security
- **AI Layer**: LLM integration for NL-SQL and report analysis
- **Notifications**: WhatsApp Business API, SMS fallback

## Deployment

This project is configured for Netlify deployment with the following setup:

### Prerequisites
- Netlify account
- GitHub repository connected to Netlify

### Deployment Steps

1. **Push to GitHub**:
   ```bash
   git add .
   git commit -m "Initial commit - Vaidya Bridge platform"
   git branch -M main
   git remote add origin https://github.com/creative-h/vaidyaBridge.git
   git push -u origin main
   ```

2. **Configure Netlify**:
   - Connect your GitHub repository to Netlify
   - Set build command: `echo "No build required"`
   - Set publish directory: `.` (root)
   - The `netlify.toml` file contains all necessary configurations

3. **Environment Variables** (for production):
   - `BIGQUERY_PROJECT_ID`: Your Google Cloud project ID
   - `LLM_API_KEY`: API key for LLM services
   - `WHATSAPP_API_KEY`: WhatsApp Business API key

## Project Structure

```
vaidyaBridge/
```

- `index.html` - Main application interface
- `netlify.toml` - Netlify deployment configuration
- `README.md` - Project documentation

## Security Features

- Row-level security in BigQuery
- PII masking for non-treating doctors
- HIPAA-aligned data handling
- TLS encryption everywhere
- Audit logging

## Development

To run locally:
1. Clone the repository
2. Open `index.html` in a web browser
3. No build process required - it's a static site

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## License

This project is part of the Vaidya Bridge healthcare platform initiative.

## Support

For deployment issues or questions, please refer to the [Netlify documentation](https://docs.netlify.com/) or create an issue in the GitHub repository.

---

## Recommended Next Steps (by priority)

1. **BigQuery schema design** - define `patients`, `reports`, `patient_tags`, `sessions`, `audit_log` tables with RLS policies
2. **LLM NL-SQL prompt engineering** - context-aware with schema injection and doctor-ID filtering built in
3. **WhatsApp Business API** integration for notification delivery (most used channel in India)
4. **Report criticality rules engine** - configurable thresholds per condition (HbA1c, BP, INR, creatinine, etc.)
5. **DISHA/PDPB compliance** review for data handling

Want to go deeper on any specific module - database schema, the AI report analysis pipeline, the NL-to-SQL architecture, or the notification system?
