<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Art App Download Page</title>
    <!-- Loading Tailwind CSS for utility styling -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Loading a fun, playful font for the kids' theme -->
    <link href="https://fonts.googleapis.com/css2?family=Balsamiq+Sans:wght@700&display=swap" rel="stylesheet">
    <style>
        /* Define playful color variables and shadow effect */
        :root {
            --color-pink: #FFC0CB; /* Pastel Pink */
            --color-blue: #ADD8E6; /* Baby Blue */
            --color-yellow: #FFFACD; /* Soft Yellow */
            --color-green: #98FB98; /* Mint Green */
            --shadow-pop: 0 8px 0 #DDA0DD; /* Plum for depth */
        }
        
        body {
            font-family: 'Balsamiq Sans', cursive;
            /* Cheerful gradient background */
            background-image: linear-gradient(135deg, var(--color-pink) 0%, var(--color-blue) 100%);
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            padding: 20px;
        }

        /* Styling for the main headline */
        .app-title {
            color: #4B0082; /* Indigo for contrast */
            /* Fun, stacked text shadow effect */
            text-shadow: 4px 4px 0px var(--color-yellow), 6px 6px 0px var(--color-pink);
            letter-spacing: 2px;
            font-size: 3rem; 
            animation: bounceIn 1s ease-out;
        }

        /* Styling for the primary action button */
        .fun-button {
            background-color: var(--color-green);
            color: #333;
            border: 4px solid #4B0082;
            box-shadow: var(--shadow-pop);
            transition: all 0.1s ease-in-out;
            padding: 1rem 3rem;
            font-size: 1.5rem;
            font-weight: bold;
        }

        /* Hover and Active states for the button */
        .fun-button:hover {
            background-color: var(--color-yellow);
            box-shadow: 0 4px 0 #9370DB; 
            transform: translateY(2px);
        }

        .fun-button:active {
            box-shadow: none;
            transform: translateY(6px);
        }

        /* Styling for the details container */
        .details-card {
            background-color: rgba(255, 255, 255, 0.95); /* Slightly transparent white */
            border: 5px solid var(--color-blue);
            box-shadow: var(--shadow-pop);
            animation: fadeIn 0.8s ease-out;
        }

        /* Placeholder styling for screenshots */
        .screenshot-placeholder {
            min-height: 150px;
            background-color: var(--color-yellow);
            border: 3px dashed #4B0082;
            font-size: 1.1rem;
            color: #4B0082;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        /* Background pattern (soft dots) */
        body::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-image: radial-gradient(#ffffff33 1px, transparent 1px);
            background-size: 15px 15px;
            z-index: -1;
        }

        /* Initial hidden state for the details section */
        .hidden-details {
            max-height: 0;
            overflow: hidden;
            opacity: 0;
            transition: max-height 0.8s ease-in-out, opacity 0.5s ease-in-out;
        }

        /* Visible state for the details section */
        .visible-details {
            max-height: 2000px; /* Large value to ensure content fits */
            opacity: 1;
        }
        
        /* Keyframe animations for visual appeal */
        @keyframes bounceIn {
            0% { transform: scale(0.5); opacity: 0; }
            80% { transform: scale(1.1); }
            100% { transform: scale(1); opacity: 1; }
        }
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
    </style>
</head>
<body class="p-4 sm:p-8">

    <!-- Main container centered on screen -->
    <div class="max-w-4xl w-full text-center">
        <!-- Main title -->
        <h1 class="app-title mb-10">
            Download ART APP
        </h1>

        <!-- The interactive button -->
        <button id="infoButton" 
                class="fun-button rounded-full shadow-lg mb-10 mx-auto block hover:scale-105"
                onclick="toggleAppDetails()">
            Click to Get the Fun Started! ✨
        </button>

        <!-- Application Details Section (Hidden by default) -->
        <div id="appDetails" class="hidden-details">
            <div class="details-card p-6 sm:p-10 rounded-3xl text-left">
                <h2 class="text-3xl font-extrabold text-[#D50000] mb-4 border-b-4 border-dashed border-[#FF8A80] pb-2 text-center">
                    Art App Features 🌈
                </h2>

                <!-- App description in English -->
                <p class="text-lg text-gray-700 mb-6 leading-relaxed">
                    Welcome to the most colorful drawing application designed for kids and families! The Art App offers a playful and safe environment where creativity knows no bounds. Dive into a world of vibrant colors, funny stamps, and easy-to-use tools.
                </p>

                <!-- Feature list -->
                <ul class="list-disc list-inside space-y-2 text-gray-800 text-xl font-bold mb-8 mx-auto" style="max-width: fit-content;">
                    <li class="text-[#FF5722]">🎨 **Rainbow Brushes:** Draw with swirling, multicolored strokes!</li>
                    <li class="text-[#FFC107]">⭐️ **Sticker Fun:** Add stars, clouds, and funny emojis with a tap.</li>
                    <li class="text-[#4CAF50]">💾 **Easy Saving:** Instantly save your masterpieces to your device.</li>
                    <li class="text-[#2196F3]">↩️ **Magic Undo:** Made a mistake? Just tap undo, it's that easy!</li>
                </ul>

                <h3 class="text-2xl font-bold text-[#FF8A80] mb-4 border-b-2 border-dashed border-[#FFD3B5] pb-2 text-center">
                    App Screenshots (Placeholders)
                </h3>
                
                <!-- Screenshot placeholders section -->
                <div class="grid grid-cols-1 sm:grid-cols-3 gap-6">
                    <div class="screenshot-placeholder rounded-xl p-4">
                        [Screenshot 1: Main Drawing Canvas]
                    </div>
                    <div class="screenshot-placeholder rounded-xl p-4">
                        [Screenshot 2: Sticker Tools Menu]
                    </div>
                    <div class="screenshot-placeholder rounded-xl p-4">
                        [Screenshot 3: Artwork Gallery]
                    </div>
                </div>
            </div>
        </div>

    </div>

    <script>
        const appDetails = document.getElementById('appDetails');
        const infoButton = document.getElementById('infoButton');

        // Function to toggle the visibility of the app details
        function toggleAppDetails() {
            const isHidden = appDetails.classList.contains('hidden-details');

            if (isHidden) {
                // Show details
                appDetails.classList.remove('hidden-details');
                appDetails.classList.add('visible-details');
                infoButton.textContent = "Awesome! Scroll Down to See the Fun! 🎉";
                
                // Change button style to pink (active state)
                infoButton.style.backgroundColor = 'var(--color-pink)';
                infoButton.style.boxShadow = '0 6px 0 #C2185B';
                infoButton.style.transform = 'translateY(0)';
            } else {
                // Hide details
                appDetails.classList.remove('visible-details');
                appDetails.classList.add('hidden-details');
                infoButton.textContent = "Click to Get the Fun Started! ✨";
                
                // Reset button style to green (default state)
                infoButton.style.backgroundColor = 'var(--color-green)';
                infoButton.style.boxShadow = 'var(--shadow-pop)';
                infoButton.style.transform = 'translateY(0)';
            }
        }
    </script>
</body>
</html>
