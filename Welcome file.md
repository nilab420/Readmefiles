# 1. Setup and Running the Application

### A. Create & Activate a Virtual Environment
1. **Create the Virtual Environment:**
   ```bash
   python -m venv venv
   ```
2. **Activate the Virtual Environment:**
   - **Windows (CMD or PowerShell):**
     ```bash
     venv\Scripts\activate
     ```
   - **Mac/Linux:**
     ```bash
     source venv/bin/activate
     ```

### B. Configure Environment Variables
- Create an `.env` file in your project’s root directory and add:
  ```
  GROQ_API_KEY=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
  base_url=https://4ipjlmd9ly3fs5-11434.proxy.runpod.net
  SEARCH_API_URL=https://www.searchapi.io/api/v1/search
  SERPER_API_KEY=364d026767c7e9e9a3cdacbef32929efe73abe88
  Google_jobs_api_key=6T7zHuzRinYKDrUwp9cPDEZ3
  voice_transcription_api_key=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
  url=http://127.0.0.1:9100
  ```

### C. Install Dependencies
- Run:
  ```bash
  pip install -r requirements.txt
  ```

### D. Run the Server
- Start the server with Uvicorn:
  ```bash
  uvicorn main:app --port 9100 --reload
  ```

---

# 3. API Endpoints

### A. Job Description Optimization Endpoint
- **URL:**  
  `http://127.0.0.1:9100/job/job_description`
- **Method:** `POST`
- **Sample Payload:**
  ```json
  {
    "job_title": "Software Engineer",
    "job_summary": "We are looking for a skilled Software Engineer to develop and maintain high-quality applications. The ideal candidate will have experience in full-stack development and a passion for creating scalable software solutions.",
    "key_responsibilities": [
      "Develop, test, and maintain software applications.",
      "Collaborate with cross-functional teams to define and implement new features.",
      "Ensure application performance, scalability, and security.",
      "Write clean, maintainable, and efficient code.",
      "Troubleshoot, debug, and enhance existing applications."
    ],
    "required_qualifications": [
      "Bachelor's degree in Computer Science or related field.",
      "Proficiency in Python, Java, or JavaScript.",
      "Experience with web development frameworks such as Django, React, or Angular.",
      "Knowledge of database management systems like PostgreSQL or MySQL.",
      "Strong problem-solving and analytical skills."
    ],
    "preferred_qualifications": [
      "Experience with cloud platforms such as AWS, Azure, or Google Cloud.",
      "Familiarity with CI/CD pipelines and DevOps practices.",
      "Knowledge of microservices architecture.",
      "Understanding of containerization using Docker and Kubernetes."
    ],
    "reporting_structure": "Reports directly to the Engineering Manager.",
    "employment_type": "Full-time",
    "work_environment": "Hybrid (Remote and Office-based)",
    "physical_demands": "No specific physical demands.",
    "location": "San Francisco, CA",
    "benefits": "Salary is 1000, health insurance, 401(k), paid time off, and professional development opportunities.",
    "salary": 2000
  }
  ```
### B. Job Comparison Endpoint
- **URL:**  
  `http://127.0.0.1:9100/job/compare_job`
- **Method:** `POST`
- **Sample Payload:**
  ```json
  {
    "job_title": "Software Engineer",
    "job_des": "Job Title:** Software Engineer - AI-Driven Products\n\n**Company Overview:**\nAt TechFusion Solutions, we empower businesses through cutting-edge technology and innovative solutions. As a global leader in AI-driven products, we foster a collaborative, inclusive, and growth-oriented work culture. With a presence in over 20 countries and a strong focus on sustainability, we shape the future of technology.\n\n**Job Summary:**\nWe seek a skilled Software Engineer to develop and maintain high-quality applications. The ideal candidate will have experience in full-stack development and a passion for creating scalable software solutions.\n\n**Key Responsibilities:**\n\n• Develop, test, and maintain software applications with expertise in Python, Java, or JavaScript.\n• Collaborate with cross-functional teams to define and implement new features, leveraging knowledge of database management systems like PostgreSQL or MySQL.\n• Ensure application performance, scalability, and security, with a focus on code optimization and API integration.\n• Write clean, maintainable, and efficient code, utilizing problem-solving and analytical skills.\n• Troubleshoot, debug, and enhance existing applications, with experience in cloud platforms such as AWS, Azure, or Google Cloud.\n\n**Required Qualifications:**\n\n• Bachelor's degree in Computer Science or related field.\n• Proficiency in programming languages, including Python, Java, or JavaScript.\n• Experience with web development frameworks, such as Django, React, or Angular.\n• Knowledge of database management systems, including PostgreSQL or MySQL.\n• Strong problem-solving and analytical skills.\n\n**Preferred Qualifications:**\n\n• Experience with cloud platforms, including AWS, Azure, or Google Cloud.\n• Familiarity with CI/CD pipelines and DevOps practices.\n• Knowledge of microservices architecture and containerization using Docker and Kubernetes.\n\n**Reporting Structure:**\nReports directly to the Engineering Manager.\n\n**Employment Type:**\nFull-time\n\n**Work Environment:**\nHybrid (Remote and Office-based)\n\n**Physical Demands:**\nNo specific physical demands.\n\n**Location:**\nSan Francisco, CA\n\n**Benefits and Perks:**\nSalary: $1000, health insurance, 401(k), paid time off, and professional development opportunities.\n\n**Contact Information:**\nTo apply, please submit your resume and cover letter to careers@techfusionsolutions.com. For further inquiries, contact us at (123) 456-7890 or visit our careers page at www.techfusionsolutions.com/careers."
  }
  ```

### C. Final Offer Approval Request Endpoint
- **URL:**  
  `http://127.0.0.1:9100/final_offer/approval-request/`
- **Method:** `POST`
- **Sample Payload:**
  ```json
  {
    "company": {
      "company_name": "TechCorp",
      "company_address": "123 Tech Lane, Silicon Valley, CA",
      "hr_manager_name": "John Doe",
      "hr_job_title": "HR Manager",
      "hr_contact_info": "john.doe@techcorp.com"
    },
    "candidate": {
      "candidate_name": "Alice Smith",
      "candidate_address": "456 Candidate Ave, San Francisco, CA",
      "candidate_email": "alice.smith@example.com"
    },
    "position": {
      "role_title": "Software Engineer",
      "employment_type": "Full-Time",
      "start_date": "2023-11-01",
      "work_scope": "Developing scalable web applications",
      "work_hours": "9 AM - 5 PM"
    },
    "compensation": {
      "performance_bonuses": "Annual performance bonus up to 10%",
      "stock_options": "500 shares vested over 4 years",
      "benefits": "Health insurance, 401k, paid time off",
      "benefit_tiers": "Tier 1",
      "max_salary": 150000,
      "max_bonus": 20000
    },
    "contract": {
      "confidentiality_clause": "Yes",
      "non_compete_duration": "1 year",
      "probationary_period": "3 months",
      "notice_period": "2 weeks",
      "remote_work_policy": "Hybrid"
    },
    "legal": {
      "background_check_required": true,
      "reference_check_required": true,
      "compliance_note": "Compliant with California labor laws"
    }
  }
  ```

### D. Final Offer Generation Endpoint
- **URL:**  
  `http://127.0.0.1:9100/final_offer/offer-letter/`
- **Method:** `POST`
- **Payload:**  
  The payload structure is identical to the **Final Offer Approval Request** payload.

### E. Database – Job Insertion Endpoint
- **URL:**  
  `http://127.0.0.1:9100/jobs/`
- **Method:** `POST`
- **Sample Payload:**
  ```json
  {
    "job_id": "job1aa23s",
    "input_text": "Python Developer**\n\n**Company Overview**\nAt TechFusion Solutions, a global leader in AI-driven products, we empower businesses through cutting-edge technology and innovative solutions. With a presence in over 20 countries and a strong focus on sustainability, we're shaping the future of technology. Join our mission to revolutionize industries and create meaningful impact worldwide.\n\n**Job Summary**\nWe're seeking a skilled Python Developer to join our team. As a Python Developer, you will be responsible for designing, developing, and maintaining our AI-driven products using Python programming language.\n\n**Key Responsibilities**\n\n• Design, develop, and maintain AI-driven products using Python programming language\n• Collaborate with cross-functional teams to identify and prioritize project requirements\n• Develop and implement efficient algorithms and data structures to ensure optimal performance\n• Troubleshoot and debug code to ensure high-quality deliverables\n• Stay up-to-date with industry trends and best practices in Python development\n\n**Required Qualifications**\n\n• Bachelor's degree in Computer Science, Information Technology, or related field\n• 2+ years of experience in Python development\n• Strong understanding of Python programming language and its applications\n• Experience with data structures, algorithms, and software design patterns\n• Proficiency in Agile development methodologies\n\n**Preferred Qualifications**\n\n• Experience with machine learning and deep learning frameworks such as TensorFlow, PyTorch, or Keras\n• Knowledge of cloud-based technologies such as Amazon Web Services (AWS) or Google Cloud Platform (GCP)\n• Familiarity with database management systems such as MySQL or PostgreSQL\n• Experience with testing frameworks such as Pytest or Unittest\n\n**Reporting Structure**\nReports directly to the Manager.\n\n**Employment Type**\nFull-time\n\n**Work Environment**\nRemote\n\n**Physical Demands**\nNone\n\n**Location**\nRemote\n\n**Benefits and Perks**\nSalary: $2000.0\n\n**Contact Information**\nTo apply, please submit your resume and cover letter to careers@techfusionsolutions.com. For further inquiries, contact us at (123) 456-7890 or visit our careers page at www.techfusionsolutions.com/careers.\n\n**How to Apply**\nIf you're a motivated and skilled Python Developer looking for a new challenge, we encourage you to apply. Please submit your application through our careers page or email us at careers@techfusionsolutions.com. We look forward to hearing from you!"
  }
  ```

### F. Retrieve Job Information
- **URL:**  
  `http://127.0.0.1:9100/jobs/{job_id}`
- **Method:** `GET`
- **Purpose:**  
  To fetch the job details for the specified `job_id`.



### G. Negotiation API – Negotiate Endpoint
- **URL:**  
  `http://127.0.0.1:9100/negotiation/negotiate`
- **Method:** `POST`
- **Sample Payload (Initialization):**
  ```json
  {
    "candidate_email": "candidate@example.com",
    "max_base": 100000,
    "max_bonus": 20000
  }
  ```
- **Sample Payload (Negotiation Round):**
  ```json
  {
    "candidate_email": "candidate@example.com",
    "candidate_input": "I would like a higher base salary and bonus."
  }
  ```
- **Description:**
  - **Initialization:**  
    When a negotiation is started for the first time, the request must include both `max_base` and `max_bonus`. The API creates a negotiation session and returns an initial offer calculated as 65% of the provided maximum values.
  - **Counteroffer Processing:**  
    For subsequent rounds, include a `candidate_input` message. The system processes this input using an AI agent to generate a counteroffer based on the candidate’s negotiation message.
  - **Negotiation Closure:**  
    If the candidate’s message indicates acceptance of the current offer, the negotiation is closed and the final offer details are returned.
  - **Round Limit:**  
    The negotiation process supports up to 3 rounds unless an offer is accepted prior to reaching the limit.


## Additional Endpoints: Job Extraction Sessions

These endpoints facilitate the extraction of job details from a provided context by leveraging NLP.

### H. Create a New Job Extraction Session
- **URL:**  
  `http://127.0.0.1:9100/job_extraction/sessions`
- **Method:** `POST`
- **Description:**  
  Creates a new session using the provided context. The API extracts full job details and mandatory information (`job_title`, `employment_type`, `salary`). Missing mandatory fields are listed in the response.
- **Sample Payload:**
  ```json
  {
    "context": "We are looking for a Software Engineer to join our dynamic team. The role is full-time with a competitive salary and offers a flexible, remote work environment."
  }
  ```
- **Sample Response:**
  ```json
  {
    "session_id": "a1b2c3d4-e5f6-7890-abcd-ef1234567890",
    "session_data": {
      "context": "We are looking for a Software Engineer to join our dynamic team. The role is full-time with a competitive salary and offers a flexible, remote work environment.",
      "job_details": {
        "job_title": "Software Engineer",
        "location": "Remote",
        "work_environment": "Remote",
        "physical_demands": "None"
      },
      "mandatory_info": {
        "job_title": "Software Engineer",
        "employment_type": "Full-Time",
        "salary": "Competitive"
      },
      "missing_fields": [],
      "complete": true
    }
  }
  ```

---

### I. Provide Additional Input for a Session
- **URL:**  
  `http://127.0.0.1:9100/job_extraction/sessions/{session_id}/input`
- **Method:** `POST`
- **Description:**  
  Appends additional input to an existing session and re-runs the extraction for mandatory job details.
- **Sample Payload:**
  ```json
  {
    "context": "The candidate must also have experience with Python and cloud platforms."
  }
  ```
- **Sample Response:**
  ```json
  {
    "session_id": "a1b2c3d4-e5f6-7890-abcd-ef1234567890",
    "session_data": {
      "context": "We are looking for a Software Engineer to join our dynamic team. The role is full-time with a competitive salary and offers a flexible, remote work environment. The candidate must also have experience with Python and cloud platforms.",
      "job_details": {
        "job_title": "Software Engineer",
        "location": "Remote",
        "work_environment": "Remote",
        "physical_demands": "None"
      },
      "mandatory_info": {
        "job_title": "Software Engineer",
        "employment_type": "Full-Time",
        "salary": "Competitive"
      },
      "missing_fields": [],
      "complete": true
    }
  }
  ```

---

### J. Get Session Status
- **URL:**  
  `http://127.0.0.1:9100/job_extraction/sessions/{session_id}`
- **Method:** `GET`
- **Description:**  
  Retrieves the current state of the session, including complete job details and mandatory information if extraction is complete, or a list of missing mandatory fields.
- **Sample Response:**
  ```json
  {
    "session_id": "a1b2c3d4-e5f6-7890-abcd-ef1234567890",
    "session_data": {
      "context": "We are looking for a Software Engineer to join our dynamic team...",
      "job_details": {
        "job_title": "Software Engineer",
        "location": "Remote",
        "work_environment": "Remote",
        "physical_demands": "None"
      },
      "mandatory_info": {
        "job_title": "Software Engineer",
        "employment_type": "Full-Time",
        "salary": "Competitive"
      },
      "missing_fields": [],
      "complete": true
    }
  }
  ```

---

## License

This project is licensed under the [MIT License](LICENSE).
```
