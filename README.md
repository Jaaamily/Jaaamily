<!DOCTYPE html>
<html lang="zh-TW">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>優惠碼複製</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            padding: 20px;
        }
        .button {
            padding: 10px 20px;
            background-color: #4CAF50;
            color: white;
            border: none;
            cursor: pointer;
            border-radius: 5px;
            font-size: 16px;
        }
        .button:hover {
            background-color: #45a049;
        }
        .message {
            margin-top: 10px;
            font-size: 14px;
            color: green;
        }
    </style>
</head>
<body>

    <h1>獲取優惠碼並前往網頁</h1>
    <p>點擊以下按鈕複製優惠碼，並跳轉到指定的網站：</p>

    <!-- 優惠碼輸入框 -->
    <input type="text" value="DISCOUNT2024" id="couponCode" readonly style="font-size: 18px; padding: 10px; width: 200px; text-align: center;">
    
    <!-- 按鈕 -->
    <button class="button" onclick="copyCoupon()">複製優惠碼並前往網站</button>

    <!-- 成功複製的訊息 -->
    <p id="message" class="message" style="display:none;">優惠碼已複製！將自動跳轉到網站。</p>

    <script>
        // 複製優惠碼並跳轉到指定網址
        function copyCoupon() {
            // 獲取優惠碼文本框
            var couponCode = document.getElementById("couponCode");

            // 選取文本框中的內容
            couponCode.select();
            couponCode.setSelectionRange(0, 99999);  // 針對移動設備設置

            // 複製內容
            document.execCommand("copy");

            // 顯示複製成功的訊息
            var message = document.getElementById("message");
            message.style.display = "block";

            // 跳轉到指定的網站
            setTimeout(function() {
                window.location.href = "https://www.example.com";  // 替換為你的目標網址
            }, 2000); // 兩秒後跳轉
        }
    </script>

</body>
</html>
