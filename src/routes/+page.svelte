<script>
    let height = 0;
    let weight = 0;
    let bmi = 0;
    let bmiText = "";
    let bmiClass = "";


    
    function CalculateBMI () {
        bmi = weight / (height * height);
        const resetTime = 2500;
        const ResetVar = () => {
            bmi = 0;
        }
        setTimeout(ResetVar, resetTime)
    if (bmi < 18.5) {
        bmiText = "Underweight";
        bmiClass = "Underweight";
    } else if (bmi > 18.5 && bmi < 24.9) {
        bmiText = "Normal";
        bmiClass = "Normal";
    } else if (bmi > 25 && bmi < 29.9) {
        bmiText = "Overweight";
        bmiClass = "Overweight";
    } else if (bmi > 30) {
        bmiText = "Obese";
        bmiClass = "Obese";
    }

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
                <input bind:value={height} placeholder="ex (1.5)">
            </div>
            <div class="input-container">
                <p>Weight</p>
                <input bind:value={weight} type="number" placeholder="ex (1.5)">
            </div>
            <div class="submitbutton">
                <div class="buttton">
                    <button on:click={CalculateBMI}>Calculate</button>
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
    <div class="Footer">
        <footer>Made with ❤️ by SkuliX</footer>
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
    position: relative;
    }

    .input-container {
        margin-top: 15px;
        text-align: center; /* Add this line to center-align the input and label */
    }

    .input-container input {
        width: 175px;
        height: 35px;
        border-radius: 15px;
        display: block; /* Change to block to prevent horizontal alignment issues */
        margin: 0 auto; /* Center-align the input field */
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

    .Bmi p {
        justify-content: center;
        align-items: center;
        display: flex;
        color: #fff;
        font-family: "montserrat", sans-serif;
    }

    .Footer footer {
        display: flex;
        align-items: center;
        justify-content: center;
        font-family: "montserrat", sans-serif;
        position: fixed;
        bottom: 95px;
        width: 100%;
        color: #fff;
        font-weight: 400;
        font-size: x-large;
    }

</style>