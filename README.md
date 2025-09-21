<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Deepsan Bhandari - GitHub Profile</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #0d1117, #161b22);
            color: #c9d1d9;
            line-height: 1.6;
            padding: 20px;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        header {
            text-align: center;
            padding: 60px 20px;
            position: relative;
            overflow: hidden;
        }
        
        .name-title {
            margin-bottom: 30px;
        }
        
        .animated-text {
            font-size: 3.5rem;
            font-weight: 800;
            background: linear-gradient(to right, #58a6ff, #8e6cff, #ff79c6);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            animation: gradientMove 5s infinite alternate;
            text-shadow: 0 0 15px rgba(88, 166, 255, 0.5);
        }
        
        .profession {
            font-size: 1.8rem;
            color: #58a6ff;
            margin-top: 10px;
            animation: fadeIn 2s ease-in;
        }
        
        .container {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
            margin-top: 40px;
        }
        
        .card {
            background: #161b22;
            border-radius: 10px;
            padding: 25px;
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
            border: 1px solid #30363d;
            transition: transform 0.3s ease;
        }
        
        .card:hover {
            transform: translateY(-5px);
        }
        
        .card-title {
            font-size: 1.5rem;
            color: #58a6ff;
            margin-bottom: 20px;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .skills {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            justify-content: center;
        }
        
        .skill-icon {
            display: flex;
            flex-direction: column;
            align-items: center;
            transition: transform 0.3s ease;
        }
        
        .skill-icon:hover {
            transform: scale(1.1);
        }
        
        .skill-icon i {
            font-size: 2.5rem;
            color: #58a6ff;
            margin-bottom: 8px;
        }
        
        .skill-icon span {
            font-size: 0.9rem;
        }
        
        .chart-container {
            position: relative;
            height: 250px;
            margin-top: 20px;
        }
        
        .stats-table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 20px;
        }
        
        .stats-table th, .stats-table td {
            padding: 12px 15px;
            text-align: left;
            border-bottom: 1px solid #30363d;
        }
        
        .stats-table th {
            background-color: #1c2128;
            color: #58a6ff;
        }
        
        .stats-table tr:hover {
            background-color: #1c2128;
        }
        
        .progress-bar {
            height: 8px;
            background: #30363d;
            border-radius: 4px;
            overflow: hidden;
        }
        
        .progress {
            height: 100%;
            border-radius: 4px;
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 40px;
        }
        
        .social-icon {
            font-size: 1.8rem;
            color: #c9d1d9;
            transition: color 0.3s ease, transform 0.3s ease;
        }
        
        .social-icon:hover {
            color: #58a6ff;
            transform: scale(1.2);
        }
        
        footer {
            text-align: center;
            margin-top: 60px;
            padding: 20px;
            color: #8b949e;
            font-size: 0.9rem;
            border-top: 1px solid #30363d;
        }
        
        @keyframes gradientMove {
            0% {
                background-position: 0%;
            }
            100% {
                background-position: 100%;
            }
        }
        
        @keyframes fadeIn {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        @media (max-width: 768px) {
            .container {
                grid-template-columns: 1fr;
            }
            
            .animated-text {
                font-size: 2.5rem;
            }
            
            .profession {
                font-size: 1.4rem;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="name-title">
            <h1 class="animated-text">Deepsan Bhandari</h1>
            <p class="profession">Programmer and Engineer</p>
        </div>
    </header>
    
    <div class="container">
        <div class="card">
            <h2 class="card-title"><i class="fas fa-code"></i> Programming Languages</h2>
            <div class="skills">
                <div class="skill-icon">
                    <i class="fab fa-cuttlefish"></i>
                    <span>C</span>
                </div>
                <div class="skill-icon">
                    <i class="fas fa-plus-square"></i>
                    <span>C++</span>
                </div>
                <div class="skill-icon">
                    <i class="fab fa-java"></i>
                    <span>Java</span>
                </div>
                <div class="skill-icon">
                    <i class="fas fa-leaf"></i>
                    <span>Spring Boot</span>
                </div>
                <div class="skill-icon">
                    <i class="fab fa-python"></i>
                    <span>Python</span>
                </div>
                <div class="skill-icon">
                    <i class="fab fa-js-square"></i>
                    <span>JavaScript</span>
                </div>
            </div>
        </div>
        
        <div class="card">
            <h2 class="card-title"><i class="fas fa-project-diagram"></i> Project Language Distribution</h2>
            <div class="chart-container">
                <canvas id="languageChart"></canvas>
            </div>
        </div>
        
        <div class="card">
            <h2 class="card-title"><i class="fas fa-table"></i> Project Stats</h2>
            <table class="stats-table">
                <thead>
                    <tr>
                        <th>Language</th>
                        <th>Percentage</th>
                        <th>Progress</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>Java</td>
                        <td>35%</td>
                        <td>
                            <div class="progress-bar">
                                <div class="progress" style="width: 35%; background: #f89820;"></div>
                            </div>
                        </td>
                    </tr>
                    <tr>
                        <td>JavaScript</td>
                        <td>25%</td>
                        <td>
                            <div class="progress-bar">
                                <div class="progress" style="width: 25%; background: #f0db4f;"></div>
                            </div>
                        </td>
                    </tr>
                    <tr>
                        <td>Python</td>
                        <td>20%</td>
                        <td>
                            <div class="progress-bar">
                                <div class="progress" style="width: 20%; background: #306998;"></div>
                            </div>
                        </td>
                    </tr>
                    <tr>
                        <td>C++</td>
                        <td>15%</td>
                        <td>
                            <div class="progress-bar">
                                <div class="progress" style="width: 15%; background: #659ad2;"></div>
                            </div>
                        </td>
                    </tr>
                    <tr>
                        <td>Other</td>
                        <td>5%</td>
                        <td>
                            <div class="progress-bar">
                                <div class="progress" style="width: 5%; background: #8b949e;"></div>
                            </div>
                        </td>
                    </tr>
                </tbody>
            </table>
        </div>
        
        <div class="card">
            <h2 class="card-title"><i class="fas fa-chart-line"></i> Activity Overview</h2>
            <div class="chart-container">
                <canvas id="activityChart"></canvas>
            </div>
        </div>
    </div>
    
    <div class="social-links">
        <a href="#" class="social-icon"><i class="fab fa-github"></i></a>
        <a href="#" class="social-icon"><i class="fab fa-linkedin"></i></a>
        <a href="#" class="social-icon"><i class="fab fa-twitter"></i></a>
        <a href="#" class="social-icon"><i class="fas fa-envelope"></i></a>
    </div>
    
    <footer>
        <p>© 2023 Deepsan Bhandari - Programmer and Engineer</p>
    </footer>

    <script>
        // Language Distribution Chart
        const languageCtx = document.getElementById('languageChart').getContext('2d');
        const languageChart = new Chart(languageCtx, {
            type: 'doughnut',
            data: {
                labels: ['Java', 'JavaScript', 'Python', 'C++', 'Other'],
                datasets: [{
                    data: [35, 25, 20, 15, 5],
                    backgroundColor: [
                        '#f89820',
                        '#f0db4f',
                        '#306998',
                        '#659ad2',
                        '#8b949e'
                    ],
                    borderWidth: 0,
                    hoverOffset: 15
                }]
            },
            options: {
                responsive: true,
                maintainAspectRatio: false,
                plugins: {
                    legend: {
                        position: 'right',
                        labels: {
                            color: '#c9d1d9',
                            font: {
                                size: 13
                            }
                        }
                    }
                },
                animation: {
                    animateScale: true,
                    animateRotate: true
                }
            }
        });
        
        // Activity Chart
        const activityCtx = document.getElementById('activityChart').getContext('2d');
        const activityChart = new Chart(activityCtx, {
            type: 'bar',
            data: {
                labels: ['Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun', 'Jul', 'Aug', 'Sep', 'Oct', 'Nov', 'Dec'],
                datasets: [{
                    label: 'Commits',
                    data: [12, 19, 7, 15, 22, 18, 25, 16, 14, 20, 17, 23],
                    backgroundColor: '#58a6ff',
                    borderRadius: 5,
                    borderWidth: 0
                }]
            },
            options: {
                responsive: true,
                maintainAspectRatio: false,
                scales: {
                    y: {
                        beginAtZero: true,
                        grid: {
                            color: 'rgba(48, 54, 61, 0.5)'
                        },
                        ticks: {
                            color: '#8b949e'
                        }
                    },
                    x: {
                        grid: {
                            color: 'rgba(48, 54, 61, 0.5)'
                        },
                        ticks: {
                            color: '#8b949e'
                        }
                    }
                },
                plugins: {
                    legend: {
                        labels: {
                            color: '#c9d1d9'
                        }
                    }
                }
            }
        });
        
        // Add animation to elements on scroll
        document.addEventListener('DOMContentLoaded', function() {
            const cards = document.querySelectorAll('.card');
            cards.forEach((card, index) => {
                card.style.animation = `fadeIn 0.5s ease ${index * 0.2}s forwards`;
                card.style.opacity = 0;
            });
        });
    </script>
</body>
</html>
