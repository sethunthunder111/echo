# Echo - Your AI Storyteller 📖✨

Echo is a smart, conversational diary app that turns your daily chats into beautifully written, narrative-style journal entries. It's designed to make journaling feel less like a chore and more like catching up with your best friend.


*(Feel free to replace this with your own screenshot!)*

## 🚀 About The Project

Tired of staring at a blank page? Echo solves that. It's a web application built with Next.js and powered by the Google Gemini API. You interact with an AI persona with a witty, modern personality. Throughout the day, you can chat with it, send text, and even upload images.

At the end of the day, when you tell the AI you're done, it takes your entire conversation and weaves it into a cohesive story, complete with a creative chapter title and subtitle, mimicking a real-life saga. Your entire history is saved in your browser, ready for you to revisit or export at any time.

## ✨ Core Features

*   **Conversational AI:** Chat with an AI bestie that has a vibrant, Gen Z-inspired personality.
*   **Narrative Story Generation:** Automatically transforms raw chat logs into beautifully formatted story chapters.
*   **Multimodal Inputs:** Supports both text and image uploads in your conversations.
*   **Persistent Client-Side History:** All your stories and the chats that created them are saved securely in your browser's `localStorage`.
*   **Secure API Key Handling:** Prompts for your Gemini API key and stores it locally. The key is passed directly to the app's backend proxy, never exposing it to client-side code during API calls.
*   **Dynamic UI:** Built with **shadcn/ui** for a clean, professional, and responsive user experience.
*   **Smooth Animations:** Subtle animations from **react-spring** bring the interface to life.
*   **Data Portability:** Export your entire journal (stories, chats, and profile) to a JSON file with a single click.

## 🛠️ Tech Stack

This project is built with a modern, full-stack JavaScript architecture:

*   **Framework:** [Next.js](https://nextjs.org/) (App Router)
*   **Styling:** [Tailwind CSS](https://tailwindcss.com/)
*   **UI Components:** [shadcn/ui](https://ui.shadcn.com/)
*   **Animations:** [react-spring](https://www.react-spring.dev/)
*   **State Management:** [Zustand](https://github.com/pmndrs/zustand)
*   **Icons:** [Lucide React](https://lucide.dev/)
*   **AI Model:** [Google Gemini API](https://ai.google.dev/)

---

## 🏁 Getting Started

To get a local copy up and running, follow these simple steps.

### Prerequisites

You will need the following installed on your machine:
*   [Node.js](https://nodejs.org/en/) (v18.x or later)
*   [npm](https://www.npmjs.com/) (usually comes with Node.js)

You will also need a **Google Gemini API Key**.
*   You can get a free key from [Google AI Studio](https://aistudio.google.com/app/apikey).

### Installation & Setup

1.  **Clone the repository:**
    ```sh
    git clone https://github.com/your-username/echo-diary-app.git
    ```
2.  **Navigate to the project directory:**
    ```sh
    cd echo-diary-app
    ```
3.  **Install NPM packages:**
    ```sh
    npm install
    ```
4.  **Run the application:**
    ```sh
    npm run dev
    ```

5.  Open your browser and navigate to [http://localhost:3000](http://localhost:3000). The app will immediately prompt you for your Gemini API Key. Paste it in, and you're ready to go!

---

## 📁 Project Structure

The project uses the Next.js App Router, which organizes the application logically:

```
/
├── app/
│   ├── api/                # Backend API routes (chat, generate-story, onboard)
│   │   └── ...
│   ├── (main)/             # Main app pages and layout
│   │   ├── page.js         # The home page (main controller)
│   │   ├── story/          # The story viewer page
│   │   └── layout.js
│   └── globals.css
├── components/
│   ├── ui/                 # Auto-generated shadcn/ui components
│   ├── ApiKeyDialog.js     # The initial API key prompt
│   ├── ChatInterface.js    # The main chat component
│   └── ...
├── lib/
│   ├── store.js            # Zustand store for state management
│   └── utils.js            # shadcn/ui utility functions
└── ...
```

## 🚀 Deployment

This application is ready for deployment on [Vercel](https://vercel.com/), the platform from the creators of Next.js.

1.  **Push your code to a GitHub repository.**
2.  **Sign up for a free account on Vercel** and connect it to your GitHub.
3.  **Import your project** from the GitHub repository.
4.  Vercel will auto-detect the Next.js framework. **No additional configuration is needed.**
5.  Click **"Deploy"**.

Vercel will build and deploy your application, providing you with a live URL. Since the app is designed for users to provide their own API keys, you **do not need to configure any server-side environment variables.**

## 🔮 Future Roadmap

This project has a strong foundation, but there's always room for growth. Here are some potential next steps:

-   [ ] **User Authentication:** Integrate NextAuth.js or Clerk to allow users to sign up and have accounts.
-   [ ] **Cloud Database Integration:** Move from `localStorage` to a cloud database like Firebase Firestore or Supabase to enable multi-device sync.
-   [ ] **Long-Term Memory:** Implement a vector database (e.g., Pinecone) to give the AI true long-term memory of past conversations.
-   [ ] **Proactive Insights:** Add weekly or monthly summaries generated by the AI to help users reflect on their patterns.
-   [ ] **Push Notifications:** Add opt-in daily reminders to encourage consistent journaling.

---

## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.
