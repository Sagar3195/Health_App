### End to End Nutritionist Generative AI Doctor Using Google Gemini and Streamlit

🥗 Gemini Health Management App
AI-Powered Calorie & Nutrition Analyzer Using Google Gemini + Streamlit

This application is an AI-driven Health & Nutrition Management App that uses Google Gemini Model (gemini-2.5-flash) to analyze food images and estimate calories, food items, and their nutritional breakdown.

Users can upload any food image, and the app intelligently identifies each item and provides a detailed calorie report — all through a simple Streamlit web interface.

📌 Features
🔹 AI Food Item Recognition

Uploads a food image and identifies every visible food item.

🔹 Calorie Estimation

The Gemini model provides:

- Total calorie count

- Per-item calorie details

- A clean, structured nutrition breakdown

🔹 Text + Image Prompting

The model receives:

- A nutrition expert prompt

- The uploaded image

- Additional user input (optional instructions)

🔹 Simple Streamlit Interface

- Image uploader

- Input text prompt

- “Tell me the total calories” button

- AI nutrition breakdown displayed instantly

| Tool                                    | Purpose                   |
| --------------------------------------- | ------------------------- |
| **Google Gemini (google-generativeai)** | Vision + text analysis    |
| **Streamlit**                           | Web application interface |
| **Pdf2Image**                           | Image processing          |
| **dotenv**                              | Secure API key loading    |
| **Python 3.10+**                        | Backend logic             |


⚙️ Getting Started
1️⃣ Clone the Repository
```bash
git clone <your_repo_url>
cd <respository_name>
```

📦 Installation Using uv Package Manager
2️⃣ Install uv (if not installed)
```bash
pip install uv
```

3️⃣ Create virtual environment
```bash
uv venv
```

4️⃣ Activate the environment

Mac/Linux
```bash
source .venv/bin/activate
```

Windows
```bash
.venv\Scripts\activate
```

5️⃣ Install dependencies
```bash
uv pip install -r requirements.txt
```

🔑 Set Up Google Gemini API Key

Create a .env file in the project root:
```bash
GOOGLE_API_KEY="YOUR_GOOGLE_API_KEY"
```

### How to Get Your Google Gemini API Key

1. Visit: https://aistudio.google.com

2. Sign in

3. Go to API Keys

4. Create an API Key

5. Copy & paste it into .env

▶️ Running the Application

Start the Streamlit app:
```bash
streamlit run app.py
```
This will open the AI Nutritionist interface in your browser.

🧪 How to Use

1. Upload a food image (JPG, JPEG, PNG).

2. Enter an optional text prompt (e.g., “Check only vegetarian items”).

3. Click Tell me the total calories.

4. View:

 - Total calories

 - Per-food-item calorie list

 - AI-generated nutritional insights

🧩 Code Explanation
🔹 get_gemini_response()

Sends:

- nutrition prompt

- uploaded food image

- optional user text

- to the gemini-2.5-flash model and returns the text output.

🔹 input_image_setup()

- Prepares uploaded images as required by Gemini.

🔹 Streamlit UI

- File uploader

- Image preview

- Prompt input

- Button for analysis

- Output display

📄 Example Output
```markdown
1. Banana – 105 calories
2. Peanut Butter Toast – 210 calories
3. Almonds – 140 calories
--------------------------------
Total Estimated Calories: 455
```
