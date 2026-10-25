ScamShield — Pause. Check. Stay Safe.

About the Project

ScamShield is a simple digital safety project that helps people identify common signs of online scams and make safer decisions.

We often receive messages claiming that our bank account will be blocked, that we have won a prize, or that we must click a link immediately. Sometimes, it is difficult to tell whether these messages are genuine or attempts to steal our personal information and money.

ScamShield aims to make this easier. Users can paste a suspicious SMS or message into the website and receive a clear warning along with practical safety advice. The project is designed for everyone, especially elderly people, first-time smartphone users, and those who may not be familiar with online scams.

Key Features

Message Checking: Scans pasted messages for common signs of online scams.

Simple Explanations: Explains why a message may look suspicious and what the user should do next.

Language Support: Provides demonstration responses in English and Tamil.

Voice Support: Reads the result aloud using the browser's speech feature, where supported.

Sample Messages: Allows users to try the website with example messages and understand how it works.

Cybercrime Reporting: Provides a direct link to India's official cybercrime reporting portal.

Mobile-Friendly Design: Works on modern mobile phones, tablets, and desktop browsers.

Technologies Used

- HTML: Creates the basic structure of the website.
- CSS: Makes the website attractive, clear, and easy to use.
- JavaScript: Handles message checking and user interactions.
- Browser Speech Synthesis: Provides optional voice output.
- GitHub Pages: Allows the website to be hosted and accessed online.

The current prototype uses simple text-matching rules to identify possible scam indicators. It does not yet use a trained AI model or a live URL reputation service.

Getting Started

Option 1: Run the Project Locally

You only need a modern web browser and a text editor to get started.

1. Download or clone the ScamShield repository from GitHub.
2. Find the "index.html" file.
3. Open the file in Chrome, Edge, Firefox, or another modern browser.
4. Paste a suspicious message into the text box.
5. Choose English or Tamil and click Check Message.
6. Try the sample messages and voice feature to explore the available functions.

The current prototype does not require any package installation or API keys.

Option 2: Run the Project Using GitHub Pages

You can publish the website online using GitHub Pages.

1. Upload "index.html" to the root folder of your GitHub repository.
2. Open the repository and go to Settings.
3. Select Pages.
4. Under the build and deployment section, choose Deploy from a branch.
5. Select the "main" branch and the "/(root)" folder.
6. Click Save and wait for GitHub Pages to finish publishing the website.
7. Open the published URL displayed in the Pages settings.

Once deployment is complete, you can share the website with others so they can try the ScamShield demo.

Environment Variables

Current Prototype

The current version runs entirely in the browser. Therefore, it does not require environment variables, API keys, or a backend server.

Planned Backend Integration

In future versions, ScamShield may include a Python FastAPI backend, an AI service, and a trusted URL reputation service. These features may require environment variables such as:

Variable| Purpose
"APP_ENV"| Identifies the environment, such as development or production.
"AI_API_KEY"| Allows the backend to access a configured AI service.
"URL_REPUTATION_API_KEY"| Allows the backend to access a configured URL reputation service.

These variables are examples for future development and are not required for the current website.

If a backend is added, create a local ".env" file using the variable names required by the implementation. For example:

APP_ENV=development
AI_API_KEY=your_ai_api_key_here
URL_REPUTATION_API_KEY=your_url_api_key_here

Replace the example values with valid credentials only after the relevant services have been configured.

Security reminder: Never place secret API keys in browser-side JavaScript or upload real credentials to a public GitHub repository. Keep sensitive keys on the backend and add ".env" to ".gitignore".

Testing the Prototype

The following sample messages can be used to understand how the current rule-based checker works.

Test 1: Suspicious Bank Message

Sample message:

«URGENT! Your bank account will be blocked today. Click this link immediately and enter your OTP and PIN to keep your account active.»

Expected result: A high-risk warning because the message contains several common scam indicators, including urgency and requests for sensitive banking information.

Test 2: Possible Prize Scam

Sample message:

«Congratulations! You have won a cash prize. Pay a small processing fee now to claim your reward.»

Expected result: A warning about unexpected prize claims and requests for payment.

Test 3: Normal Message

Sample message:

«Hi! We will meet at 5 PM near the library. Please let me know when you arrive.»

Expected result: No obvious scam indicators are detected by the current rules.

These examples are intended for demonstration and testing. The results depend on the rules implemented in the prototype, and the checker cannot identify every scam. A message that receives no warning may still be fraudulent.

Project Structure

The repository can be organised as follows:

scamshield/
├── index.html
├── README.md
├── LICENSE
├── TECHNICAL_DESIGN.md
├── sample-data/
│   └── test-cases.json
└── .env.example

The README, licence, technical design document, sample test cases, and environment example should be added to the repository as the project develops. The current website can run independently using "index.html".

Safety and Limitations

ScamShield is designed to support safer online decisions, but users should still take precautions when dealing with unexpected messages.

- Never share your OTP, UPI PIN, password, or banking details with unknown people.
- Avoid clicking unexpected links, even when a message appears to come from an official organisation.
- Verify important requests through your bank's official app, website, or verified phone number.
- Do not assume that a message is genuine just because the website does not flag it.
- Remember that the current prototype does not check URLs in real time or connect directly to banking systems.

If you suspect cybercrime in India, you can visit the official reporting portal:

https://cybercrime.gov.in/

Future Improvements

ScamShield can be improved further by adding features such as:

- Connecting the website to a Python FastAPI backend.
- Integrating an AI model to analyse messages more effectively.
- Adding trusted URL reputation checks to identify potentially dangerous links.
- Improving support for Tamil and other regional languages.
- Introducing secure screenshot analysis to check suspicious messages shared as images.
- Making cybercrime reporting guidance easier to understand.
- Expanding the sample dataset and testing the system against different types of scams.

These improvements would help make ScamShield more useful, accessible, and reliable for everyday users.

License

This project is developed for learning, demonstration, and hackathon purposes. Please refer to the "LICENSE" file in the repository for the terms and conditions governing the reuse and distribution of the code.

Conclusion

ScamShield aims to make online safety easier for everyone to understand. By helping people recognise suspicious messages, understand common scam tactics, and learn what to do next, the project encourages safer digital habits and greater confidence when using online services.

ScamShield — Pause. Check. Stay Safe.
