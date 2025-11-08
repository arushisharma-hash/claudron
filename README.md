Cauldron - An AI Idea Incubator for Students

Team: Witchware
Team Members: Akshitha Maruru, Arushi Sharma, Prathigya Malla

Abstract

Many innovative ideas from university students fail to move beyond the "what if" stage. "Cauldron" solves this by providing a native Android application that helps students turn raw ideas into structured summaries, privately and securely.

Our app, built tonight by modifying the mandatory Hackss boilerplate, uses the RunAnywhere SDK for 100% on-device, "serverless" AI inference. This ensures student ideas remain private and are processed instantly, even without an internet connection, fulfilling the core "private on-device idea summary" feature from our PPT.

🚀 Hackathon Submission

GitHub Repository: https://github.com/arushisharma-hash/claudron

Demo Video Link: [PASTE YOUR GOOGLE DRIVE LINK HERE] (This is mandatory as our project is a native Android app).

PPT Link: [PASTE YOUR GOOGLE DRIVE LINK TO THE PPT HERE]

Note on "Deployment Link"

Per the submission rules, "Either provide the deployment link or a demo video — one of them is mandatory."

Our project is a native Android app built specifically to showcase the mandatory RunAnywhere.ai SDK, which performs on-device inference. A web deployment link is not possible for this native technology. We have provided a comprehensive demo video in its place, as per the rules.

🛠️ Tech Stack

Platform: Native Android (Kotlin)

UI: Jetpack Compose

Mandatory SDK 1: RunAnywhere.ai SDK (Used for all on-device LLM generation, model management, and inference).

Mandatory SDK 2: Firebender (Used as our AI coding assistant inside Android Studio to refactor the Hackss boilerplate, write Compose UI, and debug our ViewModel).

🏃‍♂️ How to Run This Project (Demo Video Flow)

This is the exact flow we show in our demo video:

Clone this repository and open it in Android Studio.

Build & Run the app on an Android Emulator (or physical device).

The app opens on the "Cauldron" screen. We show that the "Refine" button is disabled because no model is loaded.

Navigate to the "Models" tab using the bottom navigation bar.

Tap "Download" on a model (we use SmolLM2 360M for a fast demo).

Once downloaded, tap "Load" on the same model.

Navigate back to the "Cauldron" tab. The "Refine" button is now enabled.

Type an idea into the text box (e.g., "A tiffin delivery service for students on campus").

Tap "Refine (On-Device)".

The app shows a loading spinner, then streams the AI-generated summary 100% locally using the RunAnywhere SDK.

✅ Hackathon Requirements Met

1. Use of RunAnywhere.ai SDK

We use the SDK as the core "brain" of our app. It handles model downloading, loading, and all text generation. This is visible in:

app/src/main/java/com/runanywhere/hackss/MyApplication.kt: Registers the models.

app/src/main/java/com/runanywhere/hackss/ui/ModelsScreen.kt (from base repo): Shows the UI for downloading/loading.

app/src/main/java/com/runanywhere/hackss/ChatViewModel.kt: Listens to the loaded model and calls RunAnywhere.generate() with our custom prompt.

app/src/main/java/com/runanywhere/hackss/MainActivity.kt: Contains the navigation (MainScreen) to switch between our CauldronScreen and the ModelsScreen.

2. Use of Firebender

We used the Firebender AI assistant plugin (a mandatory tool) extensively within Android Studio to accelerate our development tonight.

Refactoring: We used Firebender's chat (Cmd+L) to understand the original MainActivity.kt file. We then used inline edit (Cmd+K) to refactor the ChatScreen composable (which was inside MainActivity.kt) into our new CauldronScreen composable.

Code Generation: We used Firebender to write the Jetpack Compose boilerplate for our new UI in MainActivity.kt (inside CauldronScreen), such as the OutlinedTextField and Button layout.

Debugging & Logic: We used Firebender to help write and debug the new "Cauldron" system prompt and state management logic inside our ChatViewModel.kt.
