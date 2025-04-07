<!DOCTYPE html>
<html dir="rtl">
<head>
    <meta charset="UTF-8">
    <title>Emoji Chat - بناتي</title>
    <link href="https://fonts.googleapis.com/css2?family=Almarai&display=swap" rel="stylesheet">
    <style>
        /* CSS */
        * {
            font-family: 'Almarai', sans-serif;
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: #ffe6f2;
            color: #8b004d;
        }

        .container {
            max-width: 600px;
            margin: 20px auto;
            padding: 15px;
        }

        .header {
            background: #ff66b3;
            padding: 15px;
            border-radius: 10px;
            text-align: center;
            margin-bottom: 20px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }

        .chat-container {
            background: white;
            border-radius: 15px;
            padding: 15px;
            height: 60vh;
            overflow-y: auto;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }

        .emoji-bar {
            display: grid;
            grid-template-columns: repeat(6, 1fr);
            gap: 10px;
            margin: 15px 0;
        }

        .emoji-btn {
            font-size: 24px;
            background: #ff99cc;
            border: none;
            border-radius: 50%;
            padding: 10px;
            cursor: pointer;
            transition: transform 0.2s;
        }

        .emoji-btn:hover {
            transform: scale(1.2);
            background: #ff80bf;
        }

        .notification-bar {
            position: fixed;
            top: -50px;
            left: 50%;
            transform: translateX(-50%);
            background: #ff3385;
            color: white;
            padding: 10px 20px;
            border-radius: 25px;
            transition: top 0.5s;
            box-shadow: 0 2px 5px rgba(0,0,0,0.2);
        }

        .message {
            background: #ffe6f2;
            padding: 10px;
            border-radius: 10px;
            margin-bottom: 10px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .message.self {
            background: #ffb3d9;
            flex-direction: row-reverse;
        }

        .timestamp {
            font-size: 0.8em;
            color: #99004d;
        }

        .username {
            font-weight: bold;
            color: #cc0066;
        }
    </style>
</head>
<body>
    <!-- HTML -->
    <div class="container">
        <div class="header">
            <h1>🌸 شات البنات 🌸</h1>
        </div>
        
        <div class="chat-container" id="chatContainer"></div>
        
        <div class="emoji-bar">
            <button class="emoji-btn" onclick="sendEmoji('🫦')">🫦</button>
            <button class="emoji-btn" onclick="sendEmoji('😠')">😠</button>
            <button class="emoji-btn" onclick="sendEmoji('🥺')">🥺</button>
            <button class="emoji-btn" onclick="sendEmoji('😆')">😆</button>
            <button class="emoji-btn" onclick="sendEmoji('🌱')">🌱</button>
            <button class="emoji-btn" onclick="sendEmoji('🐢')">🐢</button>
        </div>
        
        <div class="notification-bar" id="notification">اشعار جديد!</div>
    </div>

    <script src="https://www.gstatic.com/firebasejs/8.6.8/firebase-app.js"></script>
    <script src="https://www.gstatic.com/firebasejs/8.6.8/firebase-firestore.js"></script>
    
    <script>
        // Firebase configuration
        const firebaseConfig = {
            apiKey: "YOUR_API_KEY",
            authDomain: "YOUR_AUTH_DOMAIN",
            projectId: "YOUR_PROJECT_ID",
            storageBucket: "YOUR_STORAGE_BUCKET",
            messagingSenderId: "YOUR_SENDER_ID",
            appId: "YOUR_APP_ID"
        };

        // Initialize Firebase
        firebase.initializeApp(firebaseConfig);
        const db = firebase.firestore();

        // Get elements
        const chatContainer = document.getElementById('chatContainer');
        const notification = document.getElementById('notification');
        
        // Get username
        let username = localStorage.getItem('username') || prompt('ادخلي اسمك:');
        localStorage.setItem('username', username);

        // Real-time listener for messages
        db.collection('messages').orderBy('timestamp').onSnapshot(snapshot => {
            chatContainer.innerHTML = '';
            snapshot.forEach(doc => {
                const message = doc.data();
                const messageDiv = document.createElement('div');
                messageDiv.className = `message ${message.sender === username ? 'self' : ''}`;
                messageDiv.innerHTML = `
                    <span class="emoji">${message.emoji}</span>
                    <span class="username">${message.sender}</span>
                    <span class="timestamp">${new Date(message.timestamp).toLocaleTimeString()}</span>
                `;
                chatContainer.appendChild(messageDiv);
                showNotification(`تم استلام ايموجي جديد من ${message.sender}`);
            });
            chatContainer.scrollTop = chatContainer.scrollHeight;
        });

        // Function to send emoji
        function sendEmoji(emoji) {
            db.collection('messages').add({
                emoji: emoji,
                sender: username,
                timestamp: firebase.firestore.FieldValue.serverTimestamp()
            });
        }

        // Function to show notification
        function showNotification(text) {
            notification.textContent = text;
            notification.style.top = '20px';
            setTimeout(() => {
                notification.style.top = '-50px';
            }, 3000);
        }
    </script>
</body>
</html>
