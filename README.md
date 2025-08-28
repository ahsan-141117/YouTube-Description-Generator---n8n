# Please credit Mohammad Ahsan Hummayoun when using, sharing, or adapting this workflow

This n8n workflow streamlines the process of generating and publishing YouTube video descriptions. It solves the problem of manually writing unique and engaging descriptions for every new video, saving creators time and ensuring consistency.

Upon detecting a new video upload, this automation fetches the video's details (like title and tags). These details are then passed to an Large Language Model (LLM), which intelligently crafts a relevant and optimized description. Finally, the workflow automatically publishes this new description to your YouTube video. This ensures your videos are always well-described and optimized for discoverability from the moment they go live.

⚙️ **How it Works**
This workflow leverages the power of an LLM to automate a creative task. Here's a high-level overview of the steps:

**Trigger on New Upload:** The workflow is initiated when a new video is uploaded to your YouTube channel (likely via an RSS Feed Trigger or a YouTube Watch node).

**Fetch Video Details:** It retrieves essential information about the newly uploaded video, such as its title, existing tags, and any other relevant metadata.

**LLM Integration:** The fetched video details are sent to an LLM (e.g., via a Groq Cloud or OpenAI Chat node). The LLM processes this information to generate a comprehensive and keyword-rich video description.

**Update YouTube Video:** The generated description is then used to update the corresponding video on YouTube via a "YouTube Update Video" node.

**Notifications & Error Handling:** The workflow also includes steps for sending messages (e.g., via Gmail) to confirm successful operation or alert you of any errors, ensuring you're always informed.

🚀 **Setup and Requirements**
To get this n8n workflow up and running, you'll need:

**YouTube Credentials:** An n8n credential for YouTube, allowing the workflow to access video details and update descriptions.

**LLM API Key:** A credential for your chosen Large Language Model provider (e.g., GROQ_API_KEY for Groq Cloud, or OPENAI_API_KEY for OpenAI).

**Email Credentials (Optional):** If you're using the notification feature, an n8n credential for your email service (e.g., Gmail SMTP).

These API keys and credentials will be configured directly within their respective n8n nodes.
