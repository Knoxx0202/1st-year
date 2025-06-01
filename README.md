<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>QuickBite - Online Food Ordering System</title>
    <style>
        /* Global Styles */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: #f9f9f9;
            color: #333;
            line-height: 1.6;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Header Styles */
        header {
            background-color: #ff6b6b;
            color: white;
            padding: 20px 0;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            display: flex;
            align-items: center;
        }
        
        .logo img {
            height: 60px;
            margin-right: 15px;
        }
        
        .logo-text h1 {
            font-size: 28px;
            font-weight: 700;
        }
        
        .logo-text p {
            font-size: 14px;
            font-style: italic;
        }
        
        /* Navigation */
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav ul li {
            margin-left: 20px;
        }
        
        nav ul li a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: all 0.3s ease;
        }
        
        nav ul li a:hover {
            color: #ffe66d;
        }
        
        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(0, 0, 0, 0.6), rgba(0, 0, 0, 0.6)), url('https://images.unsplash.com/photo-1504674900247-0877df9cc836?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');
            background-size: cover;
            background-position: center;
            height: 400px;
            display: flex;
            align-items: center;
            text-align: center;
            color: white;
        }
        
        .hero-content h2 {
            font-size: 42px;
            margin-bottom: 20px;
        }
        
        .hero-content p {
            font-size: 18px;
            max-width: 700px;
            margin: 0 auto 30px;
        }
        
        .btn {
            display: inline-block;
            background-color: #ff6b6b;
            color: white;
            padding: 12px 30px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s ease;
        }
        
        .btn:hover {
            background-color: #ff5252;
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
        }
        
        /* About Section */
        .about {
            padding: 80px 0;
            background-color: white;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 50px;
        }
        
        .section-title h2 {
            font-size: 36px;
            color: #333;
            position: relative;
            display: inline-block;
            padding-bottom: 15px;
        }
        
        .section-title h2::after {
            content: '';
            position: absolute;
            width: 60px;
            height: 3px;
            background-color: #ff6b6b;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
        }
        
        .about-content {
            display: flex;
            align-items: center;
            justify-content: space-between;
            flex-wrap: wrap;
        }
        
        .about-text {
            flex: 1;
            min-width: 300px;
            padding-right: 30px;
        }
        
        .about-text h3 {
            font-size: 24px;
            margin-bottom: 20px;
            color: #ff6b6b;
        }
        
        .about-text p {
            margin-bottom: 15px;
        }
        
        .about-image {
            flex: 1;
            min-width: 300px;
            margin-top: 30px;
        }
        
        .about-image img {
            width: 100%;
            border-radius: 10px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
        }
        
        /* Flowcharts Section */
        .flowcharts {
            padding: 80px 0;
            background-color: #f5f5f5;
        }
        
        .flowchart-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 20px;
            margin-top: 40px;
        }
        
        .flowchart-card {
            background-color: white;
            border-radius: 10px;
            padding: 25px;
            text-align: center;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: all 0.3s ease;
            cursor: pointer;
        }
        
        .flowchart-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
        }
        
        .flowchart-card i {
            font-size: 40px;
            color: #ff6b6b;
            margin-bottom: 20px;
        }
        
        .flowchart-card h3 {
            font-size: 18px;
            margin-bottom: 15px;
        }
        
        /* Contact Section */
        .contact {
            padding: 80px 0;
            background-color: white;
        }
        
        .contact-info {
            display: flex;
            justify-content: space-between;
            flex-wrap: wrap;
            margin-top: 40px;
        }
        
        .contact-card {
            flex: 1;
            min-width: 250px;
            margin: 15px;
            padding: 30px;
            background-color: #f9f9f9;
            border-radius: 10px;
            text-align: center;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
        }
        
        .contact-card i {
            font-size: 30px;
            color: #ff6b6b;
            margin-bottom: 20px;
        }
        
        .contact-card h3 {
            font-size: 20px;
            margin-bottom: 15px;
        }
        
        /* Footer */
        footer {
            background-color: #333;
            color: white;
            padding: 40px 0 20px;
            text-align: center;
        }
        
        .footer-content {
            display: flex;
            justify-content: space-between;
            flex-wrap: wrap;
            margin-bottom: 30px;
        }
        
        .footer-section {
            flex: 1;
            min-width: 250px;
            margin-bottom: 20px;
            padding: 0 20px;
        }
        
        .footer-section h3 {
            font-size: 20px;
            margin-bottom: 20px;
            position: relative;
            padding-bottom: 10px;
        }
        
        .footer-section h3::after {
            content: '';
            position: absolute;
            width: 40px;
            height: 2px;
            background-color: #ff6b6b;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
        }
        
        .footer-section p {
            margin-bottom: 15px;
        }
        
        .social-links a {
            display: inline-block;
            color: white;
            margin: 0 10px;
            font-size: 20px;
            transition: all 0.3s ease;
        }
        
        .social-links a:hover {
            color: #ff6b6b;
        }
        
        .copyright {
            padding-top: 20px;
            border-top: 1px solid #444;
        }
        
        /* Modal for Flowcharts */
        .modal {
            display: none;
            position: fixed;
            z-index: 1000;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.8);
            overflow: auto;
        }
        
        .modal-content {
            background-color: #fefefe;
            margin: 5% auto;
            padding: 20px;
            border-radius: 10px;
            width: 80%;
            max-width: 900px;
            box-shadow: 0 5px 30px rgba(0, 0, 0, 0.3);
            position: relative;
        }
        
        .close {
            color: #aaa;
            position: absolute;
            top: 10px;
            right: 20px;
            font-size: 28px;
            font-weight: bold;
            cursor: pointer;
        }
        
        .close:hover {
            color: #333;
        }
        
        .modal-body {
            padding: 20px;
            text-align: center;
        }
        
        .modal-body img {
            max-width: 100%;
            height: auto;
            border-radius: 5px;
            margin-top: 20px;
            border: 1px solid #ddd;
            box-shadow: 0 0 20px rgba(0,0,0,0.1);
        }
        
        .diagram-container {
            margin: 20px 0;
            overflow-x: auto;
        }
        
        /* Responsive Styles */
        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                text-align: center;
            }
            
            nav ul {
                margin-top: 20px;
                justify-content: center;
            }
            
            nav ul li {
                margin: 0 10px;
            }
            
            .hero-content h2 {
                font-size: 32px;
            }
            
            .about-content {
                flex-direction: column;
            }
            
            .about-text {
                padding-right: 0;
                margin-bottom: 30px;
            }
            
            .modal-content {
                width: 95%;
                padding: 10px;
            }
        }
    </style>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container header-content">
            <div class="logo">
                <img src="https://via.placeholder.com/60" alt="QuickBite Logo">
                <div class="logo-text">
                    <h1>QuickBite</h1>
                    <p>Delicious food at your doorstep</p>
                </div>
            </div>
            <nav>
                <ul>
                    <li><a href="#home">Home</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#flowcharts">Flowcharts</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="container hero-content">
            <div>
                <h2>Order Your Favorite Food Online</h2>
                <p>QuickBite offers a seamless online ordering experience with fast delivery and delicious meals from your favorite local restaurants.</p>
                <a href="#" class="btn">Order Now</a>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section class="about" id="about">
        <div class="container">
            <div class="section-title">
                <h2>About Our Business</h2>
            </div>
            <div class="about-content">
                <div class="about-text">
                    <h3>Welcome to QuickBite</h3>
                    <p>QuickBite is a revolutionary online food ordering system that connects hungry customers with their favorite local restaurants. Our platform makes it easy to browse menus, place orders, and track deliveries in real-time.</p>
                    <p>Founded in 2025, QuickBite has quickly become the preferred choice for food delivery in our community. We partner with the best local restaurants to bring you a wide variety of cuisines at competitive prices.</p>
                    <p>Our mission is to simplify food ordering while supporting local businesses and providing exceptional customer service. With our user-friendly interface and fast delivery network, you'll never have to wait long for a delicious meal.</p>
                </div>
                <div class="about-image">
                    <img src="https://images.unsplash.com/photo-1555396273-367ea4eb4db5?ixlib=rb-1.2.1&auto=format&fit=crop&w=634&q=80" alt="Food delivery">
                </div>
            </div>
        </div>
    </section>

    <!-- Flowcharts Section -->
    <section class="flowcharts" id="flowcharts">
        <div class="container">
            <div class="section-title">
                <h2>System Flowcharts</h2>
            </div>
            <p style="text-align: center; margin-bottom: 30px;">Click on any flowchart below to view details and diagrams about our ordering system processes.</p>
            
            <div class="flowchart-grid">
                <div class="flowchart-card" onclick="openModal('DFD Level 0', 'This diagram shows the highest level view of the system and its interactions with external entities.', 'dfd-level0')">
                    <i class="fas fa-project-diagram"></i>
                    <h3>DFD Level 0</h3>
                    <p>Context Diagram</p>
                </div>
                
                <div class="flowchart-card" onclick="openModal('DFD Level 1', 'This diagram breaks down the main processes from Level 0 into sub-processes.', 'dfd-level1')">
                    <i class="fas fa-sitemap"></i>
                    <h3>DFD Level 1</h3>
                    <p>Main Processes</p>
                </div>
                
                <div class="flowchart-card" onclick="openModal('DFD Level 2', 'This diagram provides detailed view of specific processes from Level 1.', 'dfd-level2')">
                    <i class="fas fa-network-wired"></i>
                    <h3>DFD Level 2</h3>
                    <p>Detailed Processes</p>
                </div>
                
                <div class="flowchart-card" onclick="openModal('Deployment Flowchart', 'Shows how the system components are deployed across different hardware and locations.', 'deployment-flowchart')">
                    <i class="fas fa-server"></i>
                    <h3>Deployment Flowchart</h3>
                    <p>System Deployment</p>
                </div>
                
                <div class="flowchart-card" onclick="openModal('Opportunity Flowchart', 'Identifies potential opportunities for system improvement and expansion.', 'opportunity-flowchart')">
                    <i class="fas fa-lightbulb"></i>
                    <h3>Opportunity Flowchart</h3>
                    <p>Business Opportunities</p>
                </div>
                
                <div class="flowchart-card" onclick="openModal('Matrix Flowchart', 'Displays relationships between different system components in matrix format.', 'matrix-flowchart')">
                    <i class="fas fa-table"></i>
                    <h3>Matrix Flowchart</h3>
                    <p>Component Relationships</p>
                </div>
                
                <div class="flowchart-card" onclick="openModal('Decision Flowchart', 'Outlines the decision-making processes within the system.', 'decision-flowchart')">
                    <i class="fas fa-question-circle"></i>
                    <h3>Decision Flowchart</h3>
                    <p>Decision Processes</p>
                </div>
                
                <div class="flowchart-card" onclick="openModal('System Flowchart', 'Provides an overview of the entire system workflow.', 'system-flowchart')">
                    <i class="fas fa-cogs"></i>
                    <h3>System Flowchart</h3>
                    <p>System Overview</p>
                </div>
                
                <div class="flowchart-card" onclick="openModal('Logic Flowchart', 'Illustrates the logical flow of data and processes.', 'logic-flowchart')">
                    <i class="fas fa-brain"></i>
                    <h3>Logic Flowchart</h3>
                    <p>Logical Flow</p>
                </div>
                
                <div class="flowchart-card" onclick="openModal('Production Flowchart', 'Shows the production process from order to delivery.', 'production-flowchart')">
                    <i class="fas fa-industry"></i>
                    <h3>Production Flowchart</h3>
                    <p>Order Fulfillment</p>
                </div>
                
                <div class="flowchart-card" onclick="openModal('Process Flowchart', 'Details specific processes within the system.', 'process-flowchart')">
                    <i class="fas fa-tasks"></i>
                    <h3>Process Flowchart</h3>
                    <p>Detailed Processes</p>
                </div>
                
                <div class="flowchart-card" onclick="openModal('Ishikawa Diagram', 'Fishbone diagram showing potential causes of system issues.', 'ishikawa-diagram')">
                    <i class="fas fa-fish"></i>
                    <h3>Ishikawa Diagram</h3>
                    <p>Cause Analysis</p>
                </div>
                
                <div class="flowchart-card" onclick="openModal('HIPO Structure Diagram', 'Hierarchical Input Process Output diagram of the system.', 'hipo-diagram')">
                    <i class="fas fa-layer-group"></i>
                    <h3>HIPO Structure</h3>
                    <p>System Hierarchy</p>
                </div>
                
                <div class="flowchart-card" onclick="openModal('VTOC Diagram', 'Visual Table of Contents showing system structure.', 'vtoc-diagram')">
                    <i class="fas fa-book-open"></i>
                    <h3>VTOC Diagram</h3>
                    <p>System Structure</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section class="contact" id="contact">
        <div class="container">
            <div class="section-title">
                <h2>Contact Us</h2>
            </div>
            <div class="contact-info">
                <div class="contact-card">
                    <i class="fas fa-map-marker-alt"></i>
                    <h3>Address</h3>
                    <p>SLSU Lucena</p>
                    <p>Lucena City, 4301</p>
                </div>
                <div class="contact-card">
                    <i class="fas fa-phone"></i>
                    <h3>Phone</h3>
                    <p>+639 60373 5680</p>
                    <p>Mon-Fri: 9am-9pm</p>
                </div>
                <div class="contact-card">
                    <i class="fas fa-envelope"></i>
                    <h3>Email</h3>
                    <p>info@quickbite.com</p>
                    <p>support@quickbite.com</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-section">
                    <h3>About QuickBite</h3>
                    <p>Your trusted online food ordering platform connecting you with the best local restaurants.</p>
                </div>
                <div class="footer-section">
                    <h3>Quick Links</h3>
                    <p><a href="#home" style="color: white; text-decoration: none;">Home</a></p>
                    <p><a href="#about" style="color: white; text-decoration: none;">About</a></p>
                    <p><a href="#flowcharts" style="color: white; text-decoration: none;">Flowcharts</a></p>
                    <p><a href="#contact" style="color: white; text-decoration: none;">Contact</a></p>
                </div>
                <div class="footer-section">
                    <h3>Connect With Us</h3>
                    <div class="social-links">
                        <a href="#"><i class="fab fa-facebook"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-linkedin"></i></a>
                    </div>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; 2023 QuickBite. All rights reserved.</p>
            </div>
        </div>
    </footer>

    <!-- Modal -->
    <div id="flowchartModal" class="modal">
        <div class="modal-content">
            <span class="close" onclick="closeModal()">&times;</span>
            <div class="modal-body">
                <h2 id="modalTitle">Flowchart Title</h2>
                <p id="modalDescription">Flowchart description will appear here.</p>
                
                <div class="diagram-container">
                    <!-- Diagram images will be inserted here by JavaScript -->
                    <img id="modalDiagram" src="" alt="Flowchart Diagram" style="display: none;">
                </div>
                
                <p style="margin-top: 20px; font-style: italic;">Click outside this box or the X button to close.</p>
            </div>
        </div>
    </div>

    <!-- Hidden diagram images -->
    <div style="display: none;">
        <!-- DFD Diagrams -->
        <img id="dfd-level0" src="https://media.geeksforgeeks.org/wp-content/uploads/20200609161750/Untitled229.png?text=DFD+Level+0+Diagram" alt="DFD Level 0 Diagram">
        <img id="dfd-level1" src="https://media.geeksforgeeks.org/wp-content/uploads/20200609161854/UntitledER.png?text=DFD+Level+1+Diagram" alt="DFD Level 1 Diagram">
        <img id="dfd-level2" src="https://templates.visual-paradigm.com/repository/images/2e409d26-3345-4516-acde-c36b59fa3e0b.png?text=DFD+Level+2+Diagram" alt="DFD Level 2 Diagram">
        
        <!-- Flowchart Types -->
        <img id="deployment-flowchart" src="https://via.placeholder.com/800x500.png?text=Deployment+Flowchart" alt="Deployment Flowchart">
        <img id="opportunity-flowchart" src="https://via.placeholder.com/800x500.png?text=Opportunity+Flowchart" alt="Opportunity Flowchart">
        <img id="matrix-flowchart" src="https://via.placeholder.com/800x500.png?text=Matrix+Flowchart" alt="Matrix Flowchart">
        <img id="decision-flowchart" src="https://i.pinimg.com/736x/20/a2/f5/20a2f5d240bd6043dba7c162e6d45e9b.jpg?text=Decision+Flowchart" alt="Decision Flowchart">
        <img id="system-flowchart" src="https://via.placeholder.com/800x500.png?text=System+Flowchart" alt="System Flowchart">
        <img id="logic-flowchart" src="https://via.placeholder.com/800x500.png?text=Logic+Flowchart" alt="Logic Flowchart">
        <img id="production-flowchart" src="https://templates.visual-paradigm.com/repository/images/c0d64947-af57-4a5c-a2d1-098ce896f299.png?text=Production+Flowchart" alt="Production Flowchart">
        <img id="process-flowchart" src="https://via.placeholder.com/800x500.png?text=Process+Flowchart" alt="Process Flowchart">
        
        <!-- Other Diagrams -->
        <img id="ishikawa-diagram" src="https://via.placeholder.com/800x500.png?text=Ishikawa+Diagram" alt="Ishikawa Diagram">
        <img id="hipo-diagram" src="https://via.placeholder.com/800x500.png?text=HIPO+Diagram" alt="HIPO Diagram">
        <img id="vtoc-diagram" src="https://via.placeholder.com/800x500.png?text=VTOC+Diagram" alt="VTOC Diagram">
    </div>

    <script>
        // Modal functionality
        function openModal(title, description, diagramId) {
            document.getElementById('modalTitle').textContent = title;
            document.getElementById('modalDescription').textContent = description;
            
            // Get the diagram image and clone it to show in modal
            const diagram = document.getElementById(diagramId);
            const modalDiagram = document.getElementById('modalDiagram');
            
            // Clone the diagram and show it
            modalDiagram.src = diagram.src;
            modalDiagram.alt = diagram.alt;
            modalDiagram.style.display = 'block';
            
            // Show the modal
            document.getElementById('flowchartModal').style.display = 'block';
        }
        
        function closeModal() {
            document.getElementById('flowchartModal').style.display = 'none';
            document.getElementById('modalDiagram').style.display = 'none';
        }
        
        // Close modal when clicking outside of it
        window.onclick = function(event) {
            const modal = document.getElementById('flowchartModal');
            if (event.target == modal) {
                closeModal();
            }
        }
    </script>
</body>
</html>
