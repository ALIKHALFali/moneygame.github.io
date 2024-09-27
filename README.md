<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>مسابقات ببجي</title>
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css">
    <style>
        body {
            background: url('https://i.imgur.com/2NdLVq3.png') no-repeat center center fixed;
            background-size: cover;
            color: #fff;
            font-family: 'Arial', sans-serif;
        }

        .navbar {
            background-color: rgba(0, 0, 0, 0.7);
        }

        .hero-section {
            text-align: center;
            padding: 100px 20px;
            background: rgba(0, 0, 0, 0.5);
            margin-bottom: 30px;
        }

        .hero-section h1 {
            font-size: 2.5em;
        }

        .hero-section p {
            font-size: 1.2em;
        }

        .card {
            background-color: rgba(255, 255, 255, 0.8);
            color: #000;
        }

        footer {
            text-align: center;
            padding: 20px;
            background-color: rgba(0, 0, 0, 0.7);
            position: relative;
            width: 100%;
        }

        @media (max-width: 768px) {
            .hero-section h1 {
                font-size: 1.8em;
            }

            .hero-section p {
                font-size: 1em;
            }
        }
    </style>
</head>
<body>
    <nav class="navbar navbar-expand-lg navbar-dark">
        <a class="navbar-brand" href="#">مسابقات ببجي</a>
        <div class="collapse navbar-collapse" id="navbarNav">
            <ul class="navbar-nav">
                <li class="nav-item"><a class="nav-link" href="index.html">الرئيسية</a></li>
                <li class="nav-item"><a class="nav-link" href="competitions.html">المسابقات</a></li>
                <li class="nav-item"><a class="nav-link" href="registration.html">التسجيل</a></li>
                <li class="nav-item"><a class="nav-link" href="about.html">حول</a></li>
            </ul>
        </div>
    </nav>

    <div class="hero-section">
        <h1>مرحبا بك في عالم ببجي!</h1>
        <p>انضم إلى المسابقات وكن البطل.</p>
        <a href="registration.html" class="btn btn-primary btn-lg">تسجيل الآن</a>
        <div id="subscriberCount" class="mt-3">عدد المشتركين: <span id="count">0</span></div>
    </div>

    <div class="container">
        <h2 class="text-center mb-4">أحدث المسابقات</h2>
        <div class="row">
            <div class="col-md-4 col-sm-12 mb-4">
                <div class="card">
                    <div class="card-body">
                        <h5 class="card-title">مسابقة 1</h5>
                        <p class="card-text">تفاصيل المسابقة 1 هنا.</p>
                        <a href="#" class="btn btn-primary">المزيد</a>
                    </div>
                </div>
            </div>
            <div class="col-md-4 col-sm-12 mb-4">
                <div class="card">
                    <div class="card-body">
                        <h5 class="card-title">مسابقة 2</h5>
                        <p class="card-text">تفاصيل المسابقة 2 هنا.</p>
                        <a href="#" class="btn btn-primary">المزيد</a>
                    </div>
                </div>
            </div>
            <div class="col-md-4 col-sm-12 mb-4">
                <div class="card">
                    <div class="card-body">
                        <h5 class="card-title">مسابقة 3</h5>
                        <p class="card-text">تفاصيل المسابقة 3 هنا.</p>
                        <a href="#" class="btn btn-primary">المزيد</a>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <footer>
        <p>&copy; 2024 مسابقات ببجي. جميع الحقوق محفوظة.</p>
    </footer>

    <script src="https://code.jquery.com/jquery-3.5.1.slim.min.js"></script>
    <script src="cdn.jsdelivr.net/npm/@popperjs/core@2.5.2/dist/umd/popper.min.js"></script>
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/js/bootstrap.min.js"></script>
    <script>
        let subscriberCount = 0;
        const maxSubscribers = 100;

        document.addEventListener("DOMContentLoaded", function() {
            const registrationForm = document.getElementById('registrationForm');

            if (registrationForm) {
                registrationForm.addEventListener('submit', function(event) {
                    event.preventDefault(); // منع الإرسال الافتراضي للنموذج

                    if (subscriberCount < maxSubscribers) {
                        subscriberCount++;
                        document.getElementById('count').innerText = subscriberCount;

                        if (subscriberCount === maxSubscribers) {
                            alert('لقد وصلنا إلى الحد الأقصى من المشاركين! يجب الانتظار حتى انتهاء المباراة.');
                        }

                        registrationForm.reset(); // إعادة تعيين النموذج بعد الإرسال
                    }
                });
            }
        });
    </script>
</body>
</html>
