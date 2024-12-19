<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>RAJMAHAL The Groom Studio</title>
    <link href="https://fonts.googleapis.com/css2?family=Great+Vibes&family=Engravers+MT&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #000;
            color: #ffd700;
            margin: 0;
            padding: 0px;
        }

        header {
            text-align: center;
            padding: 20px 10px;
            color: #ffd700;
            background-color: #333;
            border-bottom: 2px solid #ffd700;
        }

        header h1 {
            font-size: 4rem;
            font-family: 'Engravers MT', serif;
            margin: 0;
            animation: fadeIn 2s ease-in;
        }

        header h2 {
            font-size: 2rem;
            font-family: 'Great Vibes', cursive;
            margin: 5px 0;
            animation: fadeIn 2s ease-in 0.5s;
        }

        @keyframes fadeIn {
            from {
                opacity: 0;
            }
            to {
                opacity: 1;
            }
        }

        nav {
            text-align: center;
            margin-bottom: 20px;
            border-bottom: 2px solid #ffd700;
            padding-bottom: 8px;
        }

        nav a {
            color: #ffd700;
            text-decoration: none;
            margin: 0 20px;
            font-weight: bold;
            font-size: 1rem;
        }

        nav a:hover {
            text-decoration: underline;
        }

        #gallery-container {
            padding: 10px;
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
        }

        #gallery-container a {
            margin: 5px;
        }

        #gallery-container img {
            width: 250px;
            height: 300px;
            border-radius: 5px;
            transition: transform 0.3s ease;
            cursor: pointer;
            box-shadow: 0 4px 6px rgba(255, 215, 0, 0.4);
        }

        #gallery-container img:hover {
            transform: scale(1.1);
            box-shadow: 0 6px 8px rgba(255, 215, 0, 0.6);
        }

        #loadMore {
            background-color: #ffd700;
            color: black;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            margin: 10px auto;
            display: block;
            text-align: center;
        }

        #loadMore:hover {
            background-color: #ffc107;
        }

        #contact {
            text-align: center;
            padding: 20px;
            background-color: #222;
            color: #ffd700;
            margin-top: 20px;
            border-top: 1px solid #ffd700;
        }

        #contact p {
            margin: 10px 0;
        }

        #contact a {
            color: #ffd700;
            text-decoration: none;
            font-weight: bold;
        }

        #contact a:hover {
            text-decoration: underline;
        }

        #about {
            padding: 2em;
            text-align: center;
            background-color: #222;
            color: #ffd700;
            animation: fadeIn 2s ease-in;
        }

        /* Contact Popup Styles */
        #contactPopup {
            display: none;
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            background-color: #333;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 6px rgba(255, 215, 0, 0.4);
            z-index: 1000;
        }
        #contactPopup h2 {
            margin-top: 0;
        }
        #contactPopup p {
            margin: 0.5em 0;
        }
        .closePopup {
            background-color: #ffd700;
            color: #000;
            border: none;
            padding: 5px 10px;
            cursor: pointer;
            font-weight: bold;
            border-radius: 5px;
        }
        .overlay {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.5);
            z-index: 999;
        }
    </style>
</head>

<body>
    <header>
        <h1>RAJMAHAL</h1>
        <h2>The Groom Studio</h2>
    </header>

    <nav aria-label="Main Navigation">
        <a href="index.html" aria-label="Home">Home</a>
        <a href="jodhpuri.html" aria-label="Jodhpuri">Jodhpuri</a>
        <a href="indo-western.html" aria-label="Indo-Western">Indo-Western</a>
        <a href="#gallery-container" id="galleryLink" aria-label="Gallery">Gallery</a>
        <a id="aboutLink" aria-label="About Us">About Us</a>
        <a id="contactLink" aria-label="Contact Us">Contact</a>
    </nav>
    
    <section id="gallery">
        <h3>Explore Our Collection</h3>
        <div id="gallery-container">
            <!-- Gallery images will dynamically load here -->
        </div>
    </section>

    <button id="loadMore">Load More</button>

    <!-- About Us Section -->
    <section id="about">
        <h2>About Us</h2>
        <p>
            At RAJMAHAL The Groom Studio, we specialize in crafting elegant ethnic wear for grooms and their families. 
            Our collection features a wide range of traditional Sherwanis, Kurtas, and bespoke accessories tailored 
            to perfection. With an emphasis on quality and tradition, we ensure that every piece embodies timeless 
            craftsmanship and modern sophistication. 
        </p>
        <p>
            Discover the perfect attire for your special day and celebrate culture with style at RAJMAHAL.
        </p>
    </section>

    <!-- Contact Popup -->
    <div id="contactPopup">
        <h2>Contact Us</h2>
        <p><strong>Phone:</strong> <a href="tel:+9218255555">9218255555</a></p>
        <p><strong>Email:</strong> <a href="mailto:contact@rajmahal.com">contact@rajmahal.com</a></p>
        <p><strong>Instagram:</strong> 
            <a href="https://www.instagram.com/rajmahal_the_groom_studio" target="_blank">@rajmahal_the_groom_studio</a>
        </p>
        <button class="closePopup">Close</button>
    </div>
    <div class="overlay"></div>

    <!-- Footer Section -->
    <footer>
        <p>&copy; 2024 RAJMAHAL The Groom Studio. All rights reserved.</p>
    </footer>

    <script>
         const images = [
            { src: "images/sherwani1.jpg", link: "profile1.html" },
            { src: "images/sherwani3.jpg", link: "profile3.html" },
            { src: "images/sherwani4.jpg", link: "profile4.html" },
            { src: "images/sherwani1.jpg", link: "profile5.html" },
            { src: "images/sherwani2.jpg", link: "profile6.html" },
            { src: "images/sherwani3.jpg", link: "profile7.html" },
            { src: "images/sherwani4.jpg", link: "profile8.html" },
            { src: "images/sherwani1.jpg", link: "profile9.html" },
            { src: "images/sherwani1.jpg", link: "profile10.html" },
            { src: "images/sherwani1.jpg", link: "profile11.html" },
            { src: "images/sherwani2.jpg", link: "profile12.html" },
            { src: "images/sherwani3.jpg", link: "profile13.html" },
            { src: "images/sherwani1.jpg", link: "profile1.html" },
            { src: "images/sherwani2.jpg", link: "profile2.html" },
            { src: "images/sherwani3.jpg", link: "profile3.html" },
            { src: "images/sherwani4.jpg", link: "profile4.html" },
            { src: "images/sherwani1.jpg", link: "profile5.html" },
            { src: "images/sherwani2.jpg", link: "profile6.html" },
            { src: "images/sherwani3.jpg", link: "profile7.html" },
            { src: "images/sherwani4.jpg", link: "profile8.html" },
            { src: "images/sherwani1.jpg", link: "profile9.html" },
            { src: "images/sherwani1.jpg", link: "profile10.html" },
            { src: "images/sherwani1.jpg", link: "profile11.html" },
            { src: "images/sherwani2.jpg", link: "profile12.html" },
            { src: "images/sherwani3.jpg", link: "profile13.html" },
            { src: "images/sherwani1.jpg", link: "profile1.html" },
            { src: "images/sherwani2.jpg", link: "profile2.html" },
            { src: "images/sherwani3.jpg", link: "profile3.html" },
            { src: "images/sherwani4.jpg", link: "profile4.html" },
            { src: "images/sherwani1.jpg", link: "profile5.html" },
            { src: "images/sherwani2.jpg", link: "profile6.html" },
            { src: "images/sherwani3.jpg", link: "profile7.html" },
            { src: "images/sherwani4.jpg", link: "profile8.html" },
            { src: "images/sherwani1.jpg", link: "profile9.html" },
            { src: "images/sherwani1.jpg", link: "profile10.html" },
            { src: "images/sherwani1.jpg", link: "profile11.html" },
            { src: "images/sherwani2.jpg", link: "profile12.html" },
            { src: "images/sherwani3.jpg", link: "profile13.html" }
            // Add more images as needed
        ];

        const galleryContainer = document.getElementById("gallery-container");
        const loadMoreButton = document.getElementById("loadMore");

        let currentIndex = 0;
        const batchSize = 4;

        function loadImages() {
            const imagesToShow = images.slice(currentIndex, currentIndex + batchSize);
            imagesToShow.forEach((imgData) => {
                const link = document.createElement("a");
                link.href = imgData.link;
                const img = document.createElement("img");
                img.src = imgData.src;
                link.appendChild(img);
                galleryContainer.appendChild(link);
            });
            currentIndex += batchSize;

            if (currentIndex >= images.length) {
                loadMoreButton.innerText = "All Loaded";
                loadMoreButton.disabled = true;
            }
        }

        loadMoreButton.addEventListener("click", loadImages);

        // Initial load (first batch of images)
        loadImages();

        // Focus on gallery when link is clicked
        document.getElementById('galleryLink').addEventListener('click', (e) => {
            e.preventDefault();
            document.getElementById('gallery').scrollIntoView({ behavior: 'smooth' });
        });

        
        // About Us scroll
        const aboutLink = document.getElementById("aboutLink");
        const aboutSection = document.getElementById("about");
        aboutLink.addEventListener("click", () => aboutSection.scrollIntoView({ behavior: "smooth" }));

        // Contact Popup
        const contactLink = document.getElementById("contactLink");
        const contactPopup = document.getElementById("contactPopup");
        const overlay = document.querySelector(".overlay");
        const closePopup = document.querySelector(".closePopup");

        contactLink.addEventListener("click", () => {
            contactPopup.style.display = "block";
            overlay.style.display = "block";
        });

        closePopup.addEventListener("click", () => {
            contactPopup.style.display = "none";
            overlay.style.display = "none";
        });

    </script>
</body>

</html>
