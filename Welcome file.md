---


---

<h1 id="setup-and-running-the-application">1. Setup and Running the Application</h1>
<h3 id="a.-create--activate-a-virtual-environment">A. Create &amp; Activate a Virtual Environment</h3>
<ol>
<li><strong>Create the Virtual Environment:</strong></li>
</ol>
<pre class=" language-bash"><code class="prism  language-bash">
python -m venv venv

</code></pre>
<ol start="2">
<li><strong>Activate the Virtual Environment:</strong></li>
</ol>
<ul>
<li><strong>Windows (CMD or PowerShell):</strong></li>
</ul>
<pre class=" language-bash"><code class="prism  language-bash">
venv\Scripts\activate

</code></pre>
<ul>
<li><strong>Mac/Linux:</strong></li>
</ul>
<pre class=" language-bash"><code class="prism  language-bash">
<span class="token function">source</span> venv/bin/activate

</code></pre>
<h3 id="b.-configure-environment-variables">B. Configure Environment Variables</h3>
<ul>
<li>Create an <code>.env</code> file in your project’s root directory and add:</li>
</ul>
<pre><code>
GROQ_API_KEY=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

base_url=https://4ipjlmd9ly3fs5-11434.proxy.runpod.net

SEARCH_API_URL=https://www.searchapi.io/api/v1/search

SERPER_API_KEY=364d026767c7e9e9a3cdacbef32929efe73abe88

Google_jobs_api_key=6T7zHuzRinYKDrUwp9cPDEZ3

voice_transcription_api_key=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

url=http://127.0.0.1:9100

</code></pre>
<h3 id="c.-install-dependencies">C. Install Dependencies</h3>
<ul>
<li>Run:</li>
</ul>
<pre class=" language-bash"><code class="prism  language-bash">
pip <span class="token function">install</span> -r requirements.txt

</code></pre>
<h3 id="d.-run-the-server">D. Run the Server</h3>
<ul>
<li>Start the server with Uvicorn:</li>
</ul>
<pre class=" language-bash"><code class="prism  language-bash">
uvicorn main:app --port 9100 --reload

</code></pre>
<hr>
<h1 id="api-endpoints">3. API Endpoints</h1>
<h3 id="a.-job-description-optimization-endpoint">A. Job Description Optimization Endpoint</h3>
<ul>
<li><strong>URL:</strong></li>
</ul>
<p><code>http://127.0.0.1:9100/job/optimize_seo</code></p>
<ul>
<li>
<p><strong>Method:</strong>  <code>POST</code></p>
</li>
<li>
<p><strong>Sample Payload:</strong></p>
</li>
</ul>
<pre class=" language-json"><code class="prism  language-json">
<span class="token punctuation">{</span>

<span class="token string">"job_title"</span><span class="token punctuation">:</span> <span class="token string">"Software Engineer"</span><span class="token punctuation">,</span>

<span class="token string">"job_summary"</span><span class="token punctuation">:</span> <span class="token string">"We are looking for a skilled Software Engineer to develop and maintain high-quality applications. The ideal candidate will have experience in full-stack development and a passion for creating scalable software solutions."</span><span class="token punctuation">,</span>

<span class="token string">"key_responsibilities"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>

<span class="token string">"Develop, test, and maintain software applications."</span><span class="token punctuation">,</span>

<span class="token string">"Collaborate with cross-functional teams to define and implement new features."</span><span class="token punctuation">,</span>

<span class="token string">"Ensure application performance, scalability, and security."</span><span class="token punctuation">,</span>

<span class="token string">"Write clean, maintainable, and efficient code."</span><span class="token punctuation">,</span>

<span class="token string">"Troubleshoot, debug, and enhance existing applications."</span>

<span class="token punctuation">]</span><span class="token punctuation">,</span>

<span class="token string">"required_qualifications"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>

<span class="token string">"Bachelor's degree in Computer Science or related field."</span><span class="token punctuation">,</span>

<span class="token string">"Proficiency in Python, Java, or JavaScript."</span><span class="token punctuation">,</span>

<span class="token string">"Experience with web development frameworks such as Django, React, or Angular."</span><span class="token punctuation">,</span>

<span class="token string">"Knowledge of database management systems like PostgreSQL or MySQL."</span><span class="token punctuation">,</span>

<span class="token string">"Strong problem-solving and analytical skills."</span>

<span class="token punctuation">]</span><span class="token punctuation">,</span>

<span class="token string">"preferred_qualifications"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>

<span class="token string">"Experience with cloud platforms such as AWS, Azure, or Google Cloud."</span><span class="token punctuation">,</span>

<span class="token string">"Familiarity with CI/CD pipelines and DevOps practices."</span><span class="token punctuation">,</span>

<span class="token string">"Knowledge of microservices architecture."</span><span class="token punctuation">,</span>

<span class="token string">"Understanding of containerization using Docker and Kubernetes."</span>

<span class="token punctuation">]</span><span class="token punctuation">,</span>

<span class="token string">"reporting_structure"</span><span class="token punctuation">:</span> <span class="token string">"Reports directly to the Engineering Manager."</span><span class="token punctuation">,</span>

<span class="token string">"employment_type"</span><span class="token punctuation">:</span> <span class="token string">"Full-time"</span><span class="token punctuation">,</span>

<span class="token string">"work_environment"</span><span class="token punctuation">:</span> <span class="token string">"Hybrid (Remote and Office-based)"</span><span class="token punctuation">,</span>

<span class="token string">"physical_demands"</span><span class="token punctuation">:</span> <span class="token string">"No specific physical demands."</span><span class="token punctuation">,</span>

<span class="token string">"location"</span><span class="token punctuation">:</span> <span class="token string">"San Francisco, CA"</span><span class="token punctuation">,</span>

<span class="token string">"benefits"</span><span class="token punctuation">:</span> <span class="token string">"Salary is 1000, health insurance, 401(k), paid time off, and professional development opportunities."</span>

<span class="token punctuation">}</span>

</code></pre>
<h3 id="b.-job-comparison-endpoint">B. Job Comparison Endpoint</h3>
<ul>
<li><strong>URL:</strong></li>
</ul>
<p><code>http://127.0.0.1:9100/job/compare_job</code></p>
<ul>
<li>
<p><strong>Method:</strong>  <code>POST</code></p>
</li>
<li>
<p><strong>Sample Payload:</strong></p>
</li>
</ul>
<pre class=" language-json"><code class="prism  language-json">
<span class="token punctuation">{</span>

<span class="token string">"job_title"</span><span class="token punctuation">:</span> <span class="token string">"Software Engineer"</span><span class="token punctuation">,</span>

<span class="token string">"job_des"</span><span class="token punctuation">:</span> <span class="token string">"Job Title:** Software Engineer - AI-Driven Products\n\n**Company Overview:**\nAt TechFusion Solutions, we empower businesses through cutting-edge technology and innovative solutions. As a global leader in AI-driven products, we foster a collaborative, inclusive, and growth-oriented work culture. With a presence in over 20 countries and a strong focus on sustainability, we shape the future of technology.\n\n**Job Summary:**\nWe seek a skilled Software Engineer to develop and maintain high-quality applications. The ideal candidate will have experience in full-stack development and a passion for creating scalable software solutions.\n\n**Key Responsibilities:**\n\n• Develop, test, and maintain software applications with expertise in Python, Java, or JavaScript.\n• Collaborate with cross-functional teams to define and implement new features, leveraging knowledge of database management systems like PostgreSQL or MySQL.\n• Ensure application performance, scalability, and security, with a focus on code optimization and API integration.\n• Write clean, maintainable, and efficient code, utilizing problem-solving and analytical skills.\n• Troubleshoot, debug, and enhance existing applications, with experience in cloud platforms such as AWS, Azure, or Google Cloud.\n\n**Required Qualifications:**\n\n• Bachelor's degree in Computer Science or related field.\n• Proficiency in programming languages, including Python, Java, or JavaScript.\n• Experience with web development frameworks, such as Django, React, or Angular.\n• Knowledge of database management systems, including PostgreSQL or MySQL.\n• Strong problem-solving and analytical skills.\n\n**Preferred Qualifications:**\n\n• Experience with cloud platforms, including AWS, Azure, or Google Cloud.\n• Familiarity with CI/CD pipelines and DevOps practices.\n• Knowledge of microservices architecture and containerization using Docker and Kubernetes.\n\n**Reporting Structure:**\nReports directly to the Engineering Manager.\n\n**Employment Type:**\nFull-time\n\n**Work Environment:**\nHybrid (Remote and Office-based)\n\n**Physical Demands:**\nNo specific physical demands.\n\n**Location:**\nSan Francisco, CA\n\n**Benefits and Perks:**\nSalary: $1000, health insurance, 401(k), paid time off, and professional development opportunities.\n\n**Contact Information:**\nTo apply, please submit your resume and cover letter to careers@techfusionsolutions.com. For further inquiries, contact us at (123) 456-7890 or visit our careers page at www.techfusionsolutions.com/careers."</span>

<span class="token punctuation">}</span>

</code></pre>
<h3 id="c.-final-offer-approval-request-endpoint">C. Final Offer Approval Request Endpoint</h3>
<ul>
<li><strong>URL:</strong></li>
</ul>
<p><code>http://127.0.0.1:9100/final_offer/approval-request/</code></p>
<ul>
<li>
<p><strong>Method:</strong>  <code>POST</code></p>
</li>
<li>
<p><strong>Sample Payload:</strong></p>
</li>
</ul>
<pre class=" language-json"><code class="prism  language-json">
<span class="token punctuation">{</span>

<span class="token string">"company"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>

<span class="token string">"company_name"</span><span class="token punctuation">:</span> <span class="token string">"TechCorp"</span><span class="token punctuation">,</span>

<span class="token string">"company_address"</span><span class="token punctuation">:</span> <span class="token string">"123 Tech Lane, Silicon Valley, CA"</span><span class="token punctuation">,</span>

<span class="token string">"hr_manager_name"</span><span class="token punctuation">:</span> <span class="token string">"John Doe"</span><span class="token punctuation">,</span>

<span class="token string">"hr_job_title"</span><span class="token punctuation">:</span> <span class="token string">"HR Manager"</span><span class="token punctuation">,</span>

<span class="token string">"hr_contact_info"</span><span class="token punctuation">:</span> <span class="token string">"john.doe@techcorp.com"</span>

<span class="token punctuation">}</span><span class="token punctuation">,</span>

<span class="token string">"candidate"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>

<span class="token string">"candidate_name"</span><span class="token punctuation">:</span> <span class="token string">"Alice Smith"</span><span class="token punctuation">,</span>

<span class="token string">"candidate_address"</span><span class="token punctuation">:</span> <span class="token string">"456 Candidate Ave, San Francisco, CA"</span><span class="token punctuation">,</span>

<span class="token string">"candidate_email"</span><span class="token punctuation">:</span> <span class="token string">"alice.smith@example.com"</span>

<span class="token punctuation">}</span><span class="token punctuation">,</span>

<span class="token string">"position"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>

<span class="token string">"role_title"</span><span class="token punctuation">:</span> <span class="token string">"Software Engineer"</span><span class="token punctuation">,</span>

<span class="token string">"employment_type"</span><span class="token punctuation">:</span> <span class="token string">"Full-Time"</span><span class="token punctuation">,</span>

<span class="token string">"start_date"</span><span class="token punctuation">:</span> <span class="token string">"2023-11-01"</span><span class="token punctuation">,</span>

<span class="token string">"work_scope"</span><span class="token punctuation">:</span> <span class="token string">"Developing scalable web applications"</span><span class="token punctuation">,</span>

<span class="token string">"work_hours"</span><span class="token punctuation">:</span> <span class="token string">"9 AM - 5 PM"</span>

<span class="token punctuation">}</span><span class="token punctuation">,</span>

<span class="token string">"compensation"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>

<span class="token string">"performance_bonuses"</span><span class="token punctuation">:</span> <span class="token string">"Annual performance bonus up to 10%"</span><span class="token punctuation">,</span>

<span class="token string">"stock_options"</span><span class="token punctuation">:</span> <span class="token string">"500 shares vested over 4 years"</span><span class="token punctuation">,</span>

<span class="token string">"benefits"</span><span class="token punctuation">:</span> <span class="token string">"Health insurance, 401k, paid time off"</span><span class="token punctuation">,</span>

<span class="token string">"benefit_tiers"</span><span class="token punctuation">:</span> <span class="token string">"Tier 1"</span><span class="token punctuation">,</span>

<span class="token string">"max_salary"</span><span class="token punctuation">:</span> <span class="token number">150000</span><span class="token punctuation">,</span>

<span class="token string">"max_bonus"</span><span class="token punctuation">:</span> <span class="token number">20000</span>

<span class="token punctuation">}</span><span class="token punctuation">,</span>

<span class="token string">"contract"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>

<span class="token string">"confidentiality_clause"</span><span class="token punctuation">:</span> <span class="token string">"Yes"</span><span class="token punctuation">,</span>

<span class="token string">"non_compete_duration"</span><span class="token punctuation">:</span> <span class="token string">"1 year"</span><span class="token punctuation">,</span>

<span class="token string">"probationary_period"</span><span class="token punctuation">:</span> <span class="token string">"3 months"</span><span class="token punctuation">,</span>

<span class="token string">"notice_period"</span><span class="token punctuation">:</span> <span class="token string">"2 weeks"</span><span class="token punctuation">,</span>

<span class="token string">"remote_work_policy"</span><span class="token punctuation">:</span> <span class="token string">"Hybrid"</span>

<span class="token punctuation">}</span><span class="token punctuation">,</span>

<span class="token string">"legal"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>

<span class="token string">"background_check_required"</span><span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>

<span class="token string">"reference_check_required"</span><span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>

<span class="token string">"compliance_note"</span><span class="token punctuation">:</span> <span class="token string">"Compliant with California labor laws"</span>

<span class="token punctuation">}</span>

<span class="token punctuation">}</span>

</code></pre>
<h3 id="d.-final-offer-generation-endpoint">D. Final Offer Generation Endpoint</h3>
<ul>
<li><strong>URL:</strong></li>
</ul>
<p><code>http://127.0.0.1:9100/final_offer/offer-letter/</code></p>
<ul>
<li>
<p><strong>Method:</strong>  <code>POST</code></p>
</li>
<li>
<p><strong>Payload:</strong></p>
</li>
</ul>
<p>The payload structure is identical to the <strong>Final Offer Approval Request</strong> payload.</p>
<h3 id="e.-database-–-job-insertion-endpoint">E. Database – Job Insertion Endpoint</h3>
<ul>
<li><strong>URL:</strong></li>
</ul>
<p><code>http://127.0.0.1:9100/jobs/</code></p>
<ul>
<li>
<p><strong>Method:</strong>  <code>POST</code></p>
</li>
<li>
<p><strong>Sample Payload:</strong></p>
</li>
</ul>
<pre class=" language-json"><code class="prism  language-json">
<span class="token punctuation">{</span>

<span class="token string">"job_id"</span><span class="token punctuation">:</span> <span class="token string">"job1aa23s"</span><span class="token punctuation">,</span>

<span class="token string">"input_text"</span><span class="token punctuation">:</span> <span class="token string">"Python Developer**\n\n**Company Overview**\nAt TechFusion Solutions, a global leader in AI-driven products, we empower businesses through cutting-edge technology and innovative solutions. With a presence in over 20 countries and a strong focus on sustainability, we're shaping the future of technology. Join our mission to revolutionize industries and create meaningful impact worldwide.\n\n**Job Summary**\nWe're seeking a skilled Python Developer to join our team. As a Python Developer, you will be responsible for designing, developing, and maintaining our AI-driven products using Python programming language.\n\n**Key Responsibilities**\n\n• Design, develop, and maintain AI-driven products using Python programming language\n• Collaborate with cross-functional teams to identify and prioritize project requirements\n• Develop and implement efficient algorithms and data structures to ensure optimal performance\n• Troubleshoot and debug code to ensure high-quality deliverables\n• Stay up-to-date with industry trends and best practices in Python development\n\n**Required Qualifications**\n\n• Bachelor's degree in Computer Science, Information Technology, or related field\n• 2+ years of experience in Python development\n• Strong understanding of Python programming language and its applications\n• Experience with data structures, algorithms, and software design patterns\n• Proficiency in Agile development methodologies\n\n**Preferred Qualifications**\n\n• Experience with machine learning and deep learning frameworks such as TensorFlow, PyTorch, or Keras\n• Knowledge of cloud-based technologies such as Amazon Web Services (AWS) or Google Cloud Platform (GCP)\n• Familiarity with database management systems such as MySQL or PostgreSQL\n• Experience with testing frameworks such as Pytest or Unittest\n\n**Reporting Structure**\nReports directly to the Manager.\n\n**Employment Type**\nFull-time\n\n**Work Environment**\nRemote\n\n**Physical Demands**\nNone\n\n**Location**\nRemote\n\n**Benefits and Perks**\nSalary: $2000.0\n\n**Contact Information**\nTo apply, please submit your resume and cover letter to careers@techfusionsolutions.com. For further inquiries, contact us at (123) 456-7890 or visit our careers page at www.techfusionsolutions.com/careers.\n\n**How to Apply**\nIf you're a motivated and skilled Python Developer looking for a new challenge, we encourage you to apply. Please submit your application through our careers page or email us at careers@techfusionsolutions.com. We look forward to hearing from you!"</span>

<span class="token punctuation">}</span>

</code></pre>
<h3 id="f.-retrieve-job-information">F. Retrieve Job Information</h3>
<ul>
<li><strong>URL:</strong></li>
</ul>
<p><code>http://127.0.0.1:9100/jobs/{job_id}</code></p>
<ul>
<li>
<p><strong>Method:</strong>  <code>GET</code></p>
</li>
<li>
<p><strong>Purpose:</strong></p>
</li>
</ul>
<p>To fetch the job details for the specified <code>job_id</code>.</p>
<h3 id="g.-negotiation-api-–-negotiate-endpoint">G. Negotiation API – Negotiate Endpoint</h3>
<ul>
<li><strong>URL:</strong></li>
</ul>
<p><code>http://127.0.0.1:9100/negotiation/negotiate</code></p>
<ul>
<li>
<p><strong>Method:</strong>  <code>POST</code></p>
</li>
<li>
<p><strong>Sample Payload (Initialization):</strong></p>
</li>
</ul>
<pre class=" language-json"><code class="prism  language-json">
<span class="token punctuation">{</span>

<span class="token string">"candidate_email"</span><span class="token punctuation">:</span> <span class="token string">"candidate@example.com"</span><span class="token punctuation">,</span>

<span class="token string">"max_base"</span><span class="token punctuation">:</span> <span class="token number">100000</span><span class="token punctuation">,</span>

<span class="token string">"max_bonus"</span><span class="token punctuation">:</span> <span class="token number">20000</span>

<span class="token punctuation">}</span>

</code></pre>
<ul>
<li><strong>Sample Payload (Negotiation Round):</strong></li>
</ul>
<pre class=" language-json"><code class="prism  language-json">
<span class="token punctuation">{</span>

<span class="token string">"candidate_email"</span><span class="token punctuation">:</span> <span class="token string">"candidate@example.com"</span><span class="token punctuation">,</span>

<span class="token string">"candidate_input"</span><span class="token punctuation">:</span> <span class="token string">"I would like a higher base salary and bonus."</span>

<span class="token punctuation">}</span>

</code></pre>
<ul>
<li>
<p><strong>Description:</strong></p>
</li>
<li>
<p><strong>Initialization:</strong></p>
</li>
</ul>
<p>When a negotiation is started for the first time, the request must include both <code>max_base</code> and <code>max_bonus</code>. The API creates a negotiation session and returns an initial offer calculated as 65% of the provided maximum values.</p>
<ul>
<li><strong>Counteroffer Processing:</strong></li>
</ul>
<p>For subsequent rounds, include a <code>candidate_input</code> message. The system processes this input using an AI agent to generate a counteroffer based on the candidate’s negotiation message.</p>
<ul>
<li><strong>Negotiation Closure:</strong></li>
</ul>
<p>If the candidate’s message indicates acceptance of the current offer, the negotiation is closed and the final offer details are returned.</p>
<ul>
<li><strong>Round Limit:</strong></li>
</ul>
<p>The negotiation process supports up to 3 rounds unless an offer is accepted prior to reaching the limit.</p>
<p>—# 1. Setup and Running the Application</p>
<h3 id="a.-create--activate-a-virtual-environment-1">A. Create &amp; Activate a Virtual Environment</h3>
<ol>
<li><strong>Create the Virtual Environment:</strong></li>
</ol>
<pre class=" language-bash"><code class="prism  language-bash">
python -m venv venv

</code></pre>
<ol start="2">
<li><strong>Activate the Virtual Environment:</strong></li>
</ol>
<ul>
<li><strong>Windows (CMD or PowerShell):</strong></li>
</ul>
<pre class=" language-bash"><code class="prism  language-bash">
venv\Scripts\activate

</code></pre>
<ul>
<li><strong>Mac/Linux:</strong></li>
</ul>
<pre class=" language-bash"><code class="prism  language-bash">
<span class="token function">source</span> venv/bin/activate

</code></pre>
<h3 id="b.-configure-environment-variables-1">B. Configure Environment Variables</h3>
<ul>
<li>Create an <code>.env</code> file in your project’s root directory and add:</li>
</ul>
<pre><code>
GROQ_API_KEY=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

base_url=https://4ipjlmd9ly3fs5-11434.proxy.runpod.net

SEARCH_API_URL=https://www.searchapi.io/api/v1/search

SERPER_API_KEY=364d026767c7e9e9a3cdacbef32929efe73abe88

Google_jobs_api_key=6T7zHuzRinYKDrUwp9cPDEZ3

voice_transcription_api_key=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

url=http://127.0.0.1:9100

</code></pre>
<h3 id="c.-install-dependencies-1">C. Install Dependencies</h3>
<ul>
<li>Run:</li>
</ul>
<pre class=" language-bash"><code class="prism  language-bash">
pip <span class="token function">install</span> -r requirements.txt

</code></pre>
<h3 id="d.-run-the-server-1">D. Run the Server</h3>
<ul>
<li>Start the server with Uvicorn:</li>
</ul>
<pre class=" language-bash"><code class="prism  language-bash">
uvicorn main:app --port 9100 --reload

</code></pre>
<hr>
<h1 id="api-endpoints-1">3. API Endpoints</h1>
<h3 id="a.-job-description-optimization-endpoint-1">A. Job Description Optimization Endpoint</h3>
<ul>
<li><strong>URL:</strong></li>
</ul>
<p><code>http://127.0.0.1:9100/job/optimize_seo</code></p>
<ul>
<li>
<p><strong>Method:</strong>  <code>POST</code></p>
</li>
<li>
<p><strong>Sample Payload:</strong></p>
</li>
</ul>
<pre class=" language-json"><code class="prism  language-json">
<span class="token punctuation">{</span>

<span class="token string">"job_title"</span><span class="token punctuation">:</span> <span class="token string">"Software Engineer"</span><span class="token punctuation">,</span>

<span class="token string">"job_summary"</span><span class="token punctuation">:</span> <span class="token string">"We are looking for a skilled Software Engineer to develop and maintain high-quality applications. The ideal candidate will have experience in full-stack development and a passion for creating scalable software solutions."</span><span class="token punctuation">,</span>

<span class="token string">"key_responsibilities"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>

<span class="token string">"Develop, test, and maintain software applications."</span><span class="token punctuation">,</span>

<span class="token string">"Collaborate with cross-functional teams to define and implement new features."</span><span class="token punctuation">,</span>

<span class="token string">"Ensure application performance, scalability, and security."</span><span class="token punctuation">,</span>

<span class="token string">"Write clean, maintainable, and efficient code."</span><span class="token punctuation">,</span>

<span class="token string">"Troubleshoot, debug, and enhance existing applications."</span>

<span class="token punctuation">]</span><span class="token punctuation">,</span>

<span class="token string">"required_qualifications"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>

<span class="token string">"Bachelor's degree in Computer Science or related field."</span><span class="token punctuation">,</span>

<span class="token string">"Proficiency in Python, Java, or JavaScript."</span><span class="token punctuation">,</span>

<span class="token string">"Experience with web development frameworks such as Django, React, or Angular."</span><span class="token punctuation">,</span>

<span class="token string">"Knowledge of database management systems like PostgreSQL or MySQL."</span><span class="token punctuation">,</span>

<span class="token string">"Strong problem-solving and analytical skills."</span>

<span class="token punctuation">]</span><span class="token punctuation">,</span>

<span class="token string">"preferred_qualifications"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>

<span class="token string">"Experience with cloud platforms such as AWS, Azure, or Google Cloud."</span><span class="token punctuation">,</span>

<span class="token string">"Familiarity with CI/CD pipelines and DevOps practices."</span><span class="token punctuation">,</span>

<span class="token string">"Knowledge of microservices architecture."</span><span class="token punctuation">,</span>

<span class="token string">"Understanding of containerization using Docker and Kubernetes."</span>

<span class="token punctuation">]</span><span class="token punctuation">,</span>

<span class="token string">"reporting_structure"</span><span class="token punctuation">:</span> <span class="token string">"Reports directly to the Engineering Manager."</span><span class="token punctuation">,</span>

<span class="token string">"employment_type"</span><span class="token punctuation">:</span> <span class="token string">"Full-time"</span><span class="token punctuation">,</span>

<span class="token string">"work_environment"</span><span class="token punctuation">:</span> <span class="token string">"Hybrid (Remote and Office-based)"</span><span class="token punctuation">,</span>

<span class="token string">"physical_demands"</span><span class="token punctuation">:</span> <span class="token string">"No specific physical demands."</span><span class="token punctuation">,</span>

<span class="token string">"location"</span><span class="token punctuation">:</span> <span class="token string">"San Francisco, CA"</span><span class="token punctuation">,</span>

<span class="token string">"benefits"</span><span class="token punctuation">:</span> <span class="token string">"Salary is 1000, health insurance, 401(k), paid time off, and professional development opportunities."</span>

<span class="token punctuation">}</span>

</code></pre>
<h3 id="b.-job-comparison-endpoint-1">B. Job Comparison Endpoint</h3>
<ul>
<li><strong>URL:</strong></li>
</ul>
<p><code>http://127.0.0.1:9100/job/compare_job</code></p>
<ul>
<li>
<p><strong>Method:</strong>  <code>POST</code></p>
</li>
<li>
<p><strong>Sample Payload:</strong></p>
</li>
</ul>
<pre class=" language-json"><code class="prism  language-json">
<span class="token punctuation">{</span>

<span class="token string">"job_title"</span><span class="token punctuation">:</span> <span class="token string">"Software Engineer"</span><span class="token punctuation">,</span>

<span class="token string">"job_des"</span><span class="token punctuation">:</span> <span class="token string">"Job Title:** Software Engineer - AI-Driven Products\n\n**Company Overview:**\nAt TechFusion Solutions, we empower businesses through cutting-edge technology and innovative solutions. As a global leader in AI-driven products, we foster a collaborative, inclusive, and growth-oriented work culture. With a presence in over 20 countries and a strong focus on sustainability, we shape the future of technology.\n\n**Job Summary:**\nWe seek a skilled Software Engineer to develop and maintain high-quality applications. The ideal candidate will have experience in full-stack development and a passion for creating scalable software solutions.\n\n**Key Responsibilities:**\n\n• Develop, test, and maintain software applications with expertise in Python, Java, or JavaScript.\n• Collaborate with cross-functional teams to define and implement new features, leveraging knowledge of database management systems like PostgreSQL or MySQL.\n• Ensure application performance, scalability, and security, with a focus on code optimization and API integration.\n• Write clean, maintainable, and efficient code, utilizing problem-solving and analytical skills.\n• Troubleshoot, debug, and enhance existing applications, with experience in cloud platforms such as AWS, Azure, or Google Cloud.\n\n**Required Qualifications:**\n\n• Bachelor's degree in Computer Science or related field.\n• Proficiency in programming languages, including Python, Java, or JavaScript.\n• Experience with web development frameworks, such as Django, React, or Angular.\n• Knowledge of database management systems, including PostgreSQL or MySQL.\n• Strong problem-solving and analytical skills.\n\n**Preferred Qualifications:**\n\n• Experience with cloud platforms, including AWS, Azure, or Google Cloud.\n• Familiarity with CI/CD pipelines and DevOps practices.\n• Knowledge of microservices architecture and containerization using Docker and Kubernetes.\n\n**Reporting Structure:**\nReports directly to the Engineering Manager.\n\n**Employment Type:**\nFull-time\n\n**Work Environment:**\nHybrid (Remote and Office-based)\n\n**Physical Demands:**\nNo specific physical demands.\n\n**Location:**\nSan Francisco, CA\n\n**Benefits and Perks:**\nSalary: $1000, health insurance, 401(k), paid time off, and professional development opportunities.\n\n**Contact Information:**\nTo apply, please submit your resume and cover letter to careers@techfusionsolutions.com. For further inquiries, contact us at (123) 456-7890 or visit our careers page at www.techfusionsolutions.com/careers."</span>

<span class="token punctuation">}</span>

</code></pre>
<h3 id="c.-final-offer-approval-request-endpoint-1">C. Final Offer Approval Request Endpoint</h3>
<ul>
<li><strong>URL:</strong></li>
</ul>
<p><code>http://127.0.0.1:9100/final_offer/approval-request/</code></p>
<ul>
<li>
<p><strong>Method:</strong>  <code>POST</code></p>
</li>
<li>
<p><strong>Sample Payload:</strong></p>
</li>
</ul>
<pre class=" language-json"><code class="prism  language-json">
<span class="token punctuation">{</span>

<span class="token string">"company"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>

<span class="token string">"company_name"</span><span class="token punctuation">:</span> <span class="token string">"TechCorp"</span><span class="token punctuation">,</span>

<span class="token string">"company_address"</span><span class="token punctuation">:</span> <span class="token string">"123 Tech Lane, Silicon Valley, CA"</span><span class="token punctuation">,</span>

<span class="token string">"hr_manager_name"</span><span class="token punctuation">:</span> <span class="token string">"John Doe"</span><span class="token punctuation">,</span>

<span class="token string">"hr_job_title"</span><span class="token punctuation">:</span> <span class="token string">"HR Manager"</span><span class="token punctuation">,</span>

<span class="token string">"hr_contact_info"</span><span class="token punctuation">:</span> <span class="token string">"john.doe@techcorp.com"</span>

<span class="token punctuation">}</span><span class="token punctuation">,</span>

<span class="token string">"candidate"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>

<span class="token string">"candidate_name"</span><span class="token punctuation">:</span> <span class="token string">"Alice Smith"</span><span class="token punctuation">,</span>

<span class="token string">"candidate_address"</span><span class="token punctuation">:</span> <span class="token string">"456 Candidate Ave, San Francisco, CA"</span><span class="token punctuation">,</span>

<span class="token string">"candidate_email"</span><span class="token punctuation">:</span> <span class="token string">"alice.smith@example.com"</span>

<span class="token punctuation">}</span><span class="token punctuation">,</span>

<span class="token string">"position"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>

<span class="token string">"role_title"</span><span class="token punctuation">:</span> <span class="token string">"Software Engineer"</span><span class="token punctuation">,</span>

<span class="token string">"employment_type"</span><span class="token punctuation">:</span> <span class="token string">"Full-Time"</span><span class="token punctuation">,</span>

<span class="token string">"start_date"</span><span class="token punctuation">:</span> <span class="token string">"2023-11-01"</span><span class="token punctuation">,</span>

<span class="token string">"work_scope"</span><span class="token punctuation">:</span> <span class="token string">"Developing scalable web applications"</span><span class="token punctuation">,</span>

<span class="token string">"work_hours"</span><span class="token punctuation">:</span> <span class="token string">"9 AM - 5 PM"</span>

<span class="token punctuation">}</span><span class="token punctuation">,</span>

<span class="token string">"compensation"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>

<span class="token string">"performance_bonuses"</span><span class="token punctuation">:</span> <span class="token string">"Annual performance bonus up to 10%"</span><span class="token punctuation">,</span>

<span class="token string">"stock_options"</span><span class="token punctuation">:</span> <span class="token string">"500 shares vested over 4 years"</span><span class="token punctuation">,</span>

<span class="token string">"benefits"</span><span class="token punctuation">:</span> <span class="token string">"Health insurance, 401k, paid time off"</span><span class="token punctuation">,</span>

<span class="token string">"benefit_tiers"</span><span class="token punctuation">:</span> <span class="token string">"Tier 1"</span><span class="token punctuation">,</span>

<span class="token string">"max_salary"</span><span class="token punctuation">:</span> <span class="token number">150000</span><span class="token punctuation">,</span>

<span class="token string">"max_bonus"</span><span class="token punctuation">:</span> <span class="token number">20000</span>

<span class="token punctuation">}</span><span class="token punctuation">,</span>

<span class="token string">"contract"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>

<span class="token string">"confidentiality_clause"</span><span class="token punctuation">:</span> <span class="token string">"Yes"</span><span class="token punctuation">,</span>

<span class="token string">"non_compete_duration"</span><span class="token punctuation">:</span> <span class="token string">"1 year"</span><span class="token punctuation">,</span>

<span class="token string">"probationary_period"</span><span class="token punctuation">:</span> <span class="token string">"3 months"</span><span class="token punctuation">,</span>

<span class="token string">"notice_period"</span><span class="token punctuation">:</span> <span class="token string">"2 weeks"</span><span class="token punctuation">,</span>

<span class="token string">"remote_work_policy"</span><span class="token punctuation">:</span> <span class="token string">"Hybrid"</span>

<span class="token punctuation">}</span><span class="token punctuation">,</span>

<span class="token string">"legal"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>

<span class="token string">"background_check_required"</span><span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>

<span class="token string">"reference_check_required"</span><span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>

<span class="token string">"compliance_note"</span><span class="token punctuation">:</span> <span class="token string">"Compliant with California labor laws"</span>

<span class="token punctuation">}</span>

<span class="token punctuation">}</span>

</code></pre>
<h3 id="d.-final-offer-generation-endpoint-1">D. Final Offer Generation Endpoint</h3>
<ul>
<li><strong>URL:</strong></li>
</ul>
<p><code>http://127.0.0.1:9100/final_offer/offer-letter/</code></p>
<ul>
<li>
<p><strong>Method:</strong>  <code>POST</code></p>
</li>
<li>
<p><strong>Payload:</strong></p>
</li>
</ul>
<p>The payload structure is identical to the <strong>Final Offer Approval Request</strong> payload.</p>
<h3 id="e.-database-–-job-insertion-endpoint-1">E. Database – Job Insertion Endpoint</h3>
<ul>
<li><strong>URL:</strong></li>
</ul>
<p><code>http://127.0.0.1:9100/jobs/</code></p>
<ul>
<li>
<p><strong>Method:</strong>  <code>POST</code></p>
</li>
<li>
<p><strong>Sample Payload:</strong></p>
</li>
</ul>
<pre class=" language-json"><code class="prism  language-json">
<span class="token punctuation">{</span>

<span class="token string">"job_id"</span><span class="token punctuation">:</span> <span class="token string">"job1aa23s"</span><span class="token punctuation">,</span>

<span class="token string">"input_text"</span><span class="token punctuation">:</span> <span class="token string">"Python Developer**\n\n**Company Overview**\nAt TechFusion Solutions, a global leader in AI-driven products, we empower businesses through cutting-edge technology and innovative solutions. With a presence in over 20 countries and a strong focus on sustainability, we're shaping the future of technology. Join our mission to revolutionize industries and create meaningful impact worldwide.\n\n**Job Summary**\nWe're seeking a skilled Python Developer to join our team. As a Python Developer, you will be responsible for designing, developing, and maintaining our AI-driven products using Python programming language.\n\n**Key Responsibilities**\n\n• Design, develop, and maintain AI-driven products using Python programming language\n• Collaborate with cross-functional teams to identify and prioritize project requirements\n• Develop and implement efficient algorithms and data structures to ensure optimal performance\n• Troubleshoot and debug code to ensure high-quality deliverables\n• Stay up-to-date with industry trends and best practices in Python development\n\n**Required Qualifications**\n\n• Bachelor's degree in Computer Science, Information Technology, or related field\n• 2+ years of experience in Python development\n• Strong understanding of Python programming language and its applications\n• Experience with data structures, algorithms, and software design patterns\n• Proficiency in Agile development methodologies\n\n**Preferred Qualifications**\n\n• Experience with machine learning and deep learning frameworks such as TensorFlow, PyTorch, or Keras\n• Knowledge of cloud-based technologies such as Amazon Web Services (AWS) or Google Cloud Platform (GCP)\n• Familiarity with database management systems such as MySQL or PostgreSQL\n• Experience with testing frameworks such as Pytest or Unittest\n\n**Reporting Structure**\nReports directly to the Manager.\n\n**Employment Type**\nFull-time\n\n**Work Environment**\nRemote\n\n**Physical Demands**\nNone\n\n**Location**\nRemote\n\n**Benefits and Perks**\nSalary: $2000.0\n\n**Contact Information**\nTo apply, please submit your resume and cover letter to careers@techfusionsolutions.com. For further inquiries, contact us at (123) 456-7890 or visit our careers page at www.techfusionsolutions.com/careers.\n\n**How to Apply**\nIf you're a motivated and skilled Python Developer looking for a new challenge, we encourage you to apply. Please submit your application through our careers page or email us at careers@techfusionsolutions.com. We look forward to hearing from you!"</span>

<span class="token punctuation">}</span>

</code></pre>
<h3 id="f.-retrieve-job-information-1">F. Retrieve Job Information</h3>
<ul>
<li><strong>URL:</strong></li>
</ul>
<p><code>http://127.0.0.1:9100/jobs/{job_id}</code></p>
<ul>
<li>
<p><strong>Method:</strong>  <code>GET</code></p>
</li>
<li>
<p><strong>Purpose:</strong></p>
</li>
</ul>
<p>To fetch the job details for the specified <code>job_id</code>.</p>
<h3 id="g.-negotiation-api-–-negotiate-endpoint-1">G. Negotiation API – Negotiate Endpoint</h3>
<ul>
<li><strong>URL:</strong></li>
</ul>
<p><code>http://127.0.0.1:9100/negotiation/negotiate</code></p>
<ul>
<li>
<p><strong>Method:</strong>  <code>POST</code></p>
</li>
<li>
<p><strong>Sample Payload (Initialization):</strong></p>
</li>
</ul>
<pre class=" language-json"><code class="prism  language-json">
<span class="token punctuation">{</span>

<span class="token string">"candidate_email"</span><span class="token punctuation">:</span> <span class="token string">"candidate@example.com"</span><span class="token punctuation">,</span>

<span class="token string">"max_base"</span><span class="token punctuation">:</span> <span class="token number">100000</span><span class="token punctuation">,</span>

<span class="token string">"max_bonus"</span><span class="token punctuation">:</span> <span class="token number">20000</span>

<span class="token punctuation">}</span>

</code></pre>
<ul>
<li><strong>Sample Payload (Negotiation Round):</strong></li>
</ul>
<pre class=" language-json"><code class="prism  language-json">
<span class="token punctuation">{</span>

<span class="token string">"candidate_email"</span><span class="token punctuation">:</span> <span class="token string">"candidate@example.com"</span><span class="token punctuation">,</span>

<span class="token string">"candidate_input"</span><span class="token punctuation">:</span> <span class="token string">"I would like a higher base salary and bonus."</span>

<span class="token punctuation">}</span>

</code></pre>
<ul>
<li>
<p><strong>Description:</strong></p>
</li>
<li>
<p><strong>Initialization:</strong></p>
</li>
</ul>
<p>When a negotiation is started for the first time, the request must include both <code>max_base</code> and <code>max_bonus</code>. The API creates a negotiation session and returns an initial offer calculated as 65% of the provided maximum values.</p>
<ul>
<li><strong>Counteroffer Processing:</strong></li>
</ul>
<p>For subsequent rounds, include a <code>candidate_input</code> message. The system processes this input using an AI agent to generate a counteroffer based on the candidate’s negotiation message.</p>
<ul>
<li><strong>Negotiation Closure:</strong></li>
</ul>
<p>If the candidate’s message indicates acceptance of the current offer, the negotiation is closed and the final offer details are returned.</p>
<ul>
<li><strong>Round Limit:</strong></li>
</ul>
<p>The negotiation process supports up to 3 rounds unless an offer is accepted prior to reaching the limit.</p>
<hr>

