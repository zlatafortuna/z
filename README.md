<!DOCTYPE html>
<html lang="uk">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Фінансове планування для стартапів | Злата Фортуна</title>
    <script src="https://cdn.jsdelivr.net/npm/react@18.2.0/umd/react.production.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/react-dom@18.2.0/umd/react-dom.production.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/@babel/standalone@7.20.15/babel.min.js"></script>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        @keyframes fadeInUp {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        .animate-fadeInUp {
            animation: fadeInUp 0.8s ease-out forwards;
        }
        .hover-scale:hover {
            transform: scale(1.05);
            transition: transform 0.3s ease;
        }
    </style>
</head>
<body>
    <div id="root"></div>
    <script type="text/babel">
        function Header() {
            return (
                <header className="bg-gradient-to-r from-blue-600 to-indigo-700 text-white py-16">
                    <div className="container mx-auto px-4 text-center">
                        <h1 className="text-4xl md:text-5xl font-bold mb-4 animate-fadeInUp">
                            Фінансове планування для стартапів
                        </h1>
                        <p className="text-xl mb-6 animate-fadeInUp" style={{ animationDelay: '0.2s' }}>
                            25.04.2025
                        </p>
                        <p className="text-lg max-w-2xl mx-auto animate-fadeInUp" style={{ animationDelay: '0.4s' }}>
                            Експерти Злата Фортуна діляться порадами щодо ефективного фінансового планування для стартапів.
                        </p>
                    </div>
                </header>
            );
        }

        function TipsSection() {
            const tips = [
                {
                    title: "Створіть реалістичний бюджет",
                    description: "Визначте ключові витрати, включаючи операційні витрати, маркетинг та розробку продукту. Використовуйте інструменти прогнозування для оцінки доходів.",
                },
                {
                    title: "Плануйте грошовий потік",
                    description: "Регулярно відстежуйте вхідні та вихідні кошти. Створіть резервний фонд для непередбачених витрат.",
                },
                {
                    title: "Залучайте інвестиції розумно",
                    description: "Шукайте інвесторів, які поділяють ваше бачення. Уникайте надмірного розведення капіталу на ранніх етапах.",
                },
                {
                    title: "Автоматизуйте фінанси",
                    description: "Використовуйте сучасні інструменти, такі як QuickBooks або Xero, для автоматизації бухгалтерії та звітності.",
                },
            ];

            return (
                <section className="py-16 bg-gray-100">
                    <div className="container mx-auto px-4">
                        <h2 className="text-3xl font-bold text-center mb-12 animate-fadeInUp">
                            Ключові поради від Злата Фортуна
                        </h2>
                        <div className="grid grid-cols-1 md:grid-cols-2 gap-8">
                            {tips.map((tip, index) => (
                                <div
                                    key={index}
                                    className="bg-white p-6 rounded-lg shadow-lg hover-scale animate-fadeInUp"
                                    style={{ animationDelay: `${0.2 * (index + 1)}s` }}
                                >
                                    <h3 className="text-xl font-semibold mb-3 text-blue-600">{tip.title}</h3>
                                    <p className="text-gray-600">{tip.description}</p>
                                </div>
                            ))}
                        </div>
                    </div>
                </section>
            );
        }

        function CallToAction() {
            return (
                <section className="bg-blue-600 text-white py-16">
                    <div className="container mx-auto px-4 text-center">
                        <h2 className="text-3xl font-bold mb-4 animate-fadeInUp">
                            Готові оптимізувати фінанси вашого стартапу?
                        </h2>
                        <p className="text-lg mb-8 animate-fadeInUp" style={{ animationDelay: '0.2s' }}>
                            Зв’яжіться з експертами Злата Фортуна для індивідуальної консультації.
                        </p>
                        <a
                            href="#"
                            className="inline-block bg-white text-blue-600 font-semibold py-3 px-8 rounded-full hover:bg-gray-100 transition animate-fadeInUp"
                            style={{ animationDelay: '0.4s' }}
                        >
                            Запланувати консультацію
                        </a>
                    </div>
                </section>
            );
        }

        function Footer() {
            return (
                <footer className="bg-gray-800 text-white py-8">
                    <div className="container mx-auto px-4 text-center">
                        <p>&copy; 2025 Злата Фортуна. Всі права захищено.</p>
                    </div>
                </footer>
            );
        }

        function App() {
            return (
                <div>
                    <Header />
                    <TipsSection />
                    <CallToAction />
                    <Footer />
                </div>
            );
        }

        const root = ReactDOM.createRoot(document.getElementById('root'));
        root.render(<App />);
    </script>
</body>
</html>
