<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>آلة حاسبة - تطبيق سطح المكتب</title>
    <link rel="stylesheet" href="style.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Cairo:wght@300;400;600;700&display=swap">
</head>
<body>
    <div class="container">
        <header class="app-header">
            <h1><i class="fas fa-calculator"></i> آلة حاسبة</h1>
            <div class="window-controls">
                <button class="win-btn" id="minimize"><i class="fas fa-window-minimize"></i></button>
                <button class="win-btn" id="maximize"><i class="fas fa-window-maximize"></i></button>
                <button class="win-btn close" id="close"><i class="fas fa-times"></i></button>
            </div>
        </header>

        <div class="calculator">
            <!-- شاشة العرض -->
            <div class="display">
                <div class="previous-operand" id="previous-operand"></div>
                <div class="current-operand" id="current-operand">0</div>
                <div class="memory-indicator" id="memory-indicator"></div>
            </div>
            
            <!-- أزرار الآلة الحاسبة -->
            <div class="buttons">
                <!-- الصف الأول -->
                <button class="btn memory-btn" data-action="memory-clear">MC</button>
                <button class="btn memory-btn" data-action="memory-recall">MR</button>
                <button class="btn memory-btn" data-action="memory-add">M+</button>
                <button class="btn memory-btn" data-action="memory-subtract">M-</button>
                <button class="btn operator" data-action="clear">C</button>
                <button class="btn operator" data-action="backspace"><i class="fas fa-backspace"></i></button>
                <button class="btn operator" data-action="divide">÷</button>
                
                <!-- الصف الثاني -->
                <button class="btn" data-number="7">7</button>
                <button class="btn" data-number="8">8</button>
                <button class="btn" data-number="9">9</button>
                <button class="btn operator" data-action="multiply">×</button>
                
                <!-- الصف الثالث -->
                <button class="btn" data-number="4">4</button>
                <button class="btn" data-number="5">5</button>
                <button class="btn" data-number="6">6</button>
                <button class="btn operator" data-action="subtract">−</button>
                
                <!-- الصف الرابع -->
                <button class="btn" data-number="1">1</button>
                <button class="btn" data-number="2">2</button>
                <button class="btn" data-number="3">3</button>
                <button class="btn operator" data-action="add">+</button>
                
                <!-- الصف الخامس -->
                <button class="btn" data-action="plus-minus">±</button>
                <button class="btn" data-number="0">0</button>
                <button class="btn" data-action="decimal">.</button>
                <button class="btn equals" data-action="equals">=</button>
            </div>
            
            <!-- العمليات المتقدمة -->
            <div class="advanced-buttons">
                <button class="btn advanced" data-action="square">x²</button>
                <button class="btn advanced" data-action="square-root">√</button>
                <button class="btn advanced" data-action="percentage">%</button>
                <button class="btn advanced" data-action="inverse">1/x</button>
            </div>
            
            <!-- حالة الذاكرة -->
            <div class="memory-status">
                <span id="memory-value">الذاكرة: 0</span>
            </div>
        </div>
        
        <footer class="app-footer">
            <p>تم التطوير باستخدام <i class="fab fa-electron"></i> Electron.js</p>
        </footer>
    </div>
    
    <script src="renderer.js"></script>
</body>
</html>
