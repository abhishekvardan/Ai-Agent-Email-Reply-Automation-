This project outlines an AI email automation workflow built with n8n, designed to automatically read incoming Gmail messages, generate professional replies using a Groq AI agent (LLaMA 3), and respond intelligently with memory and context.

### Features of the Workflow:

* **Automatic Email Processing**: The system automatically handles unread Gmail messages, streamlining communication management.
* **Intelligent Reply Generation**: It leverages Groq’s LLaMA 3 model to create intelligent and relevant email responses, ensuring high-quality communication.
* **Conversation Context Retention**: The workflow maintains memory for conversation context, allowing for more coherent and continuous interactions within email threads.
* **Professional and Polite Responses**: It sends clear, polite, and professional email replies, maintaining a consistent brand voice.
* **Flexible Automation Triggers**: The automation can be triggered manually for on-demand use or scheduled for regular, hands-free operation.
* **No-Code/Low-Code Implementation**: The entire solution is built using n8n, eliminating the need for additional backend code and simplifying deployment.

### Technologies Utilized:

The workflow integrates several key technologies to achieve its automation capabilities:

* **n8n**: Serves as the visual workflow automation platform, enabling intuitive setup and management of the entire process.
* **Gmail Node**: This component is responsible for efficiently reading incoming emails and sending out generated replies within the Gmail environment.
* **Groq Chat Model**: Utilizes the LLaMA 3 (70B model) to generate dynamic and contextually appropriate email content.
* **Langchain Agent**: Manages prompt processing and provides essential memory support, enhancing the AI's ability to understand and respond to ongoing conversations.
* **Memory Buffer**: Specifically designed to maintain thread-wise context for conversations, ensuring that replies are relevant to the entire email exchange.

### Step-by-Step Setup Guide:

1.  **Initiate n8n**: Begin by running the command `n8n start` and accessing the n8n interface through your web browser at `http://localhost:5678`.
2.  **Import the Workflow**: Import the pre-configured workflow by clicking the ☰ menu within n8n and selecting "Import Workflow," then uploading the `My_workflow.json` file from the project repository.
3.  **Configure Required Credentials**:
    * **Gmail OAuth2**: Establish a connection to your Gmail account to enable email access and sending capabilities.
    * **Groq API**: Configure the Groq API by specifying the `llama3-70b-8192` model and providing your unique Groq API key in the credentials section.
4.  **Optional: Create Gmail Label for Tracking**: Navigate to your Gmail settings and create a new label named "AI-Responded." This label is crucial for preventing the system from sending duplicate replies to emails that have already been processed.
5.  **Workflow Testing**:
    * Send a test email from an external account to your connected Gmail address. An example subject could be "Request for Leave" with a body like "Hi, I would like to request a leave for this Friday. Please confirm if that works.".
    * Within n8n, open the imported workflow and click "Execute Workflow" to run a test.
    * Verify the outcome in your Gmail: confirm the AI's generated reply in your Sent Mail, check for the "AI-Responded" label applied to the original email, and ensure the original email is marked as read.

### Functionality of the "AI-Responded" Label:

The "AI-Responded" label plays a pivotal role in preventing redundant email replies. By marking emails that have already been processed and replied to by the AI, the workflow can efficiently identify and bypass these messages in subsequent runs, ensuring that each email receives only one automated response.

### Automating the Workflow:

For fully autonomous operation, integrate a "Cron Node" at the commencement of your workflow in n8n. Configure this node to execute the workflow at regular intervals, such as every 5–10 minutes, to continuously monitor and process new incoming emails.
