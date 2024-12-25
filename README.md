
## Steps to Configure Google Colab Runtime with Ngrok and Ollama

### 1. Obtain an Ngrok Token
Ngrok allows you to expose the Colab runtime to the internet securely.
1. Go to [Ngrok's website](https://ngrok.com/).
2. Sign up for a free account.
3. After signing in, navigate to the **Dashboard**.
4. Copy your Ngrok authentication token from the dashboard.

### 2. Configure the Colab Runtime
1. Open a new notebook in Google Colab.
2. Connect to the runtime by clicking the **Connect** button in the top-right corner.

### 3. Set Up Secret Token in Colab
You need to store the Ngrok authentication token securely.

#### Install Ollama
1. Install Ollama by running the following command in a Colab code cell:
   ```
   !pip install ollama
   ```

#### Retrieve Ngrok Token
- Paste your Ngrok token in a code cell and store it as a secret:
```
import os
os.environ["NGROK_TOKEN"] = "your-ngrok-token-here"
```
