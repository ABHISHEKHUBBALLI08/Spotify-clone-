
Spotify Clone 🎵
A Spotify-inspired music streaming application built with ReactJS. This project includes dynamic album rendering, routing, and responsive UI.

📂 Project Structure
plaintext
Copy code


spotify-clone/
├── dist/                  # Build files (if applicable)
├── node_modules/          # Project dependencies
├── public/
│   ├── index.html         # Main HTML file
├── src/
│   ├── assets/
│   │   ├── assets.js      # Album data (e.g., album colors, details)
│   ├── components/
│   │   ├── AlbumItem.js   # Individual album rendering logic
│   │   ├── Display.js     # Main Display component for dynamic views
│   │   ├── DisplayHome.js # Homepage content rendering
│   │   ├── DisplayAlbum.js # Album detail page logic
│   │   ├── Navbar.js      # Navigation bar
│   │   ├── Sidebar.js     # Sidebar menu
│   │   ├── SongItem.js    # Individual song details
│   ├── context/
│   │   ├── PlayerContext.js # Context for global player state
│   ├── App.js             # Main application file
│   ├── index.css          # Global styling
│   ├── main.jsx           # Entry point for React
├── .gitignore             # Ignored files for Git
├── package.json           # Project metadata and dependencies


✨ Features
Dynamic Album Rendering

Background changes dynamically based on album color (bgColor from albumsData).
Routing Integration

Home page (/) and Album details (/album/:id) are dynamically rendered using React Router.
Responsive UI

Styled components for a seamless user experience across devices.
🛠️ Libraries and Dependencies
The following packages are required to run this project:

ReactJS: Core framework


npm install react react-dom
React Router DOM: For navigation

npm install react-router-dom
Styled Components: For custom styling


npm install styled-components
Optional Dependencies (if required):

react-icons: For additional icons
axios: For API integration
framer-motion: For animations
🚀 How to Run
Clone the repository:


git clone https://github.com/ABHISHEKHUBBALLI08/Spotify-clone.git
cd spotify-clone
Install dependencies:


npm install
Start the development server:

npm start
Open the application in your browser:


http://localhost:3000
🌈 Dynamic Display Logic
The Display.js component dynamically changes the background color based on the album. Here's how it works:

Code Snippet:

jsx

const bgColor = albumsData[Number(albumId)].bgColor;
useEffect(() => {
  if (isAlbum) {
    displayRef.current.style.background = `linear-gradient(${bgColor}, #121212)`;
  } else {
    displayRef.current.style.background = `#121212`;
  }
});
Routes:

/: Renders DisplayHome
/album/:id: Renders DisplayAlbum
