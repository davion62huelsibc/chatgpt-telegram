
# ChatGPT Bot  

**Interact with ChatGPT via Telegram**  

This is a CLI tool that powers a Telegram bot, letting you interact with ChatGPT—a large language model trained by OpenAI.  

---

## Installation  

### Step 1: Download  

1. Go to the [Releases Page](../../releases).  
2. Download the file for your operating system:  
    - **macOS (Intel):** `chatgpt-telegram-Darwin-amd64`  
    - **macOS (M1):** `chatgpt-telegram-Darwin-arm64`  
    - **Linux (x64):** `chatgpt-telegram-Linux-amd64`  
    - **Linux (ARM):** `chatgpt-telegram-Linux-arm64`  
    - **Windows:** `chatgpt-telegram-Win-amd64`  

3. Extract the file into a folder.  

---

### Step 2: Configure  

1. Open the `env.example` file in a text editor and fill in the required fields:  
    - **`TELEGRAM_TOKEN`:** Your Telegram Bot token.  
    - **`TELEGRAM_ID` (Optional):** Your Telegram User ID.  
      If set, only you can interact with the bot. To get your ID, message [@userinfobot](https://t.me/userinfobot) on Telegram. You can list multiple IDs separated by commas.  
    - **`EDIT_WAIT_SECONDS` (Optional):** Time to wait between edits (default is `1 second`). Increase if you encounter "Too Many Requests" errors.  

2. Save the file and rename it to **`.env`**.  
   > **Note:** Ensure the file is named **exactly** `.env`. The program won't work otherwise.  

---

### Step 3: Run  

1. Navigate to the folder where you extracted the file.  
   - **Windows:** Use PowerShell to navigate. For example:  
     ```bash
     cd C:\path\to\chatgpt-telegram
     ```  
   - **Mac/Linux:** Use the terminal with the `cd` command.  

2. Run the bot:  
   ```bash
   ./chatgpt-telegram
   ```  

---

## Authentication  

When running the program for the first time, it will open a browser for you to log in to your ChatGPT account. Once logged in, the browser will close automatically, and the bot will be ready to use.  

If the browser-based login doesn't work for you (e.g., running on a server without a screen), you can manually provide your ChatGPT session token. Here's how:  

1. Log in to ChatGPT in your browser.  
2. Open **Developer Tools** (right-click anywhere on the page → Inspect).  
3. Go to the **Application** tab → **Cookies** section.  
4. Copy the value of the `__Secure-next-auth.session-token` cookie.  
5. Create a file named `chatgpt.json` in the appropriate folder for your OS:  
    - **Windows:** `C:\Users\YOUR_USERNAME_HERE\AppData\Roaming\chatgpt.json`  
    - **Linux:** `~/.config/chatgpt.json`  
    - **macOS:** `/Users/YOUR_USERNAME_HERE/Library/Application Support/chatgpt.json`  
6. Add the following content to the file:  
   ```json
   { "openaisession": "YOUR_COOKIE_HERE" }
   ```  

---

Now your ChatGPT Telegram bot is ready to use! 
