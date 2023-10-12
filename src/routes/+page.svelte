<script>
    let height = 0;
    let weight = 0;
    let bmi = 0;
    let bmiText = "";
    let bmiClass = "";

    function CalculateBMI () {
        calc = 
    }
    

</script>


<body>
    <div class="TextDiv">
        <div class="Section1">
            <h1>BMI Calculator</h1>
        </div>
    </div>
    <div class="Forms">
        <div class="Section2">
            <div class="input-container">
                <p>Height</p>
                <input bind:value={height} type="number">
            </div>
            <div class="input-container">
                <p>Weight</p>
                <input bind:value={weight} type="number">
            </div>
            <div class="submitbutton">
                <div class="buttton">
                    <button>Calculate</button>
                </div>
            </div>
            <div class="bmitext">
                <div class="Bmi">
                    <p>Your bmi is : {bmiText}</p>
                    <p>And you are classified : {bmiClass}</p>
                </div>
            </div>
        </div>
    </div>
</body>

<style>

    @import url('https://fonts.googleapis.com/css2?family=Lato:wght@100;300;400;700;900&family=Montserrat:wght@400;700&display=swap');
    @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@100;200;300;400;500;600;700;800;900&display=swap');

    body {
        height: 100%;
        background-color: #0F0E0E;
        margin: 0;
    }

    .TextDiv {
        height: 100%;
        width: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .Section1 h1 {
        color: #fff;
        font-family: 'montserrat', sans-serif;
        font-weight: 300;
    }

    .Forms {
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    }

    .input-container {
        margin-top: 15px;
    }

    .input-container input {
        width: 175px;
        height: 35px;
        border-radius: 15px;
    }

    .input-container p {
        align-items: center;
        display: flex;
        justify-content: center;
        color: #fff;
        font-family: "montserrat", sans-serif;
    }


    .submitbutton {
        justify-content: center;
        align-items: center;
        display: flex;
        margin-top: 25px;
    }

    .buttton button {
        border: none;
        font-family: "montserrat", sans-serif;
        width: 125px;
        height: 45px;
        border-radius: 15px;
        animation-name: fadeoutBtn;
        animation-duration: 1s;
        animation-fill-mode: backwards;
    }

    .buttton button:hover {
        animation-name: fadeinBtn;
        animation-duration: 1s;
        animation-fill-mode: forwards;
    }

    @keyframes fadeinBtn {
        from {
            background-color: #fff;
        }
        to {
            transition: background-color 0.5s ease;
            background-color: #3282B8;
        }
    }

    @keyframes fadeoutBtn {
        from {
            background-color: #3282B8;
        }
        to {
            transition: background-color 0.5s ease;
            background-color: #fff;
        }
    }
</style>