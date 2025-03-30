



    <div id="welcome-container">
        <div id="welcome-left">
            <img src="stonks-man.png" alt="" id="stonks-man" draggable="false">
        </div>
        <div id="welcome-rigth">
            <img src="stonksCraft-logo.png" alt="" id="stonksCraft-logo" draggable="false">
            <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Aspernatur aut id perferendis inventore numquam dolores qui porro perspiciatis, iure amet labore eligendi tempore, provident sit omnis, laborum itaque eos libero? Lorem ipsum dolor sit amet consectetur adipisicing elit. Inventore, dignissimos consequatur repudiandae maxime ratione temporibus modi, omnis molestiae deleniti impedit quaerat et! Ex incidunt fugiat minima, ab molestiae libero quisquam.</p>
            <button id="copy-ip-btn">📋 COPY SERVER IP</button>
        </div>
    </div>


<style>
    #welcome-container {
        width: 100%;
        height: 800px;
        display: flex;
        justify-content: space-around;
        align-items: center;
        overflow: hidden;
        
        background-image: url("./walcome-background.png");
        background-size: cover;   /* Dopasowuje tło jak object-fit: cover */
        background-position: center; /* Wycentrowanie tła */
        background-repeat: no-repeat; /* Zapobiega powtarzaniu */
        overflow: hidden;
    }

    #stonks-man{
        z-index: 90;
        position: relative;
        padding-bottom: 78px;
        transform: scale(1.75);
    }

    #welcome-left{
        height: 100%;
        width: 35%;
        display: flex;
        justify-content: center;
        align-items: flex-end;
    }

    #welcome-rigth{
        height: 100%;
        width: 65%;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: space-evenly;
    }

    p {
        position: relative;
        background: rgba(255, 255, 255, 0.1);
        padding: 40px 50px;
        border-radius: 8px;
        color: white;
        font-size: 1.5rem;
        font-family: 'Minecraft', sans-serif;
        text-align: center;
        margin: 0;
        z-index: 1;
    }

    p::before {
        content: "";
        position: absolute;
        top: -10px; left: -10px; right: -10px; bottom: -10px;
        background: inherit;
        backdrop-filter: blur(15px);
        border-radius: 16px;
        z-index: -1;
        opacity: 0.7;
        filter: blur(10px);
    }

    #stonksCraft-logo{
        padding-top: 25px;
        width: 65%;
        min-width: 450px;
    }





    @keyframes glow {
        0% { box-shadow: 0 0 5px rgba(255, 255, 255, 0.2); }
        50% { box-shadow: 0 0 15px rgba(255, 255, 255, 0.5); }
        100% { box-shadow: 0 0 5px rgba(255, 255, 255, 0.2); }
    }

    #copy-ip-btn {
        z-index: 100;
        background: url("https://static.wikia.nocookie.net/minecraft_gamepedia/images/0/09/Blue_Concrete_Powder_(texture)_JE1_BE1.png");
        background-size: cover;
        color: white;
        font-size: 2rem;
        font-weight: bold;
        font-family: 'Minecraft', sans-serif;
        padding: 12px 24px;
        border: 2px solid #444;
        border-radius: 8px;
        cursor: pointer;
        transition: all 0.3s ease;
        text-transform: uppercase;
        letter-spacing: 1px;
        outline: none;
        box-shadow: 0 4px 10px rgba(255, 255, 255, 0.2);
    }

    #copy-ip-btn:hover {
        background: url("https://static.wikia.nocookie.net/minecraft_gamepedia/images/9/9a/Light_Blue_Concrete_Powder_%28texture%29_JE1_BE1.png");
        background-size: cover;
        filter: brightness(1.2);
        animation: glow 1s infinite alternate;
        transform: translateY(-2px);
    }

    #copy-ip-btn:active {
        transform: scale(0.95);
        box-shadow: 0 2px 5px rgba(255, 255, 255, 0.2);
    }




    @media (max-width: 1200px) {
        #welcome-left{
            display: none;
        }
        #welcome-rigth{
            width: 100%;
        }
    }
</style>