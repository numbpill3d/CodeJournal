import React, { useState } from 'react';
import './App.css';

function App() {
    const [isPoweredOn, setIsPoweredOn] = useState(false);

    const handlePowerOn = () => {
        setIsPoweredOn(true);
    };

    return (
        <div className="cyber-app">
            {!isPoweredOn ? (
                <div className="power-screen">
                    <h1 className="title">CyberJournal</h1>
                    <img
                        src="assets/book.gif"
                        alt="Closed Book"
                        className="book-image"
                    />
                    <button className="power-button" onClick={handlePowerOn}>
                        Power On
                    </button>
                </div>
            ) : (
                <div className="book-container">
                    <div className="page left-page">
                        <h2>Page 1</h2>
                        <p>Welcome to your CyberJournal. This is your left page.</p>
                    </div>
                    <div className="page right-page">
                        <h2>Page 2</h2>
                        <p>Explore your notes and code snippets on the right page.</p>
                    </div>
                </div>
            )}
        </div>
    );
}

export default App;
