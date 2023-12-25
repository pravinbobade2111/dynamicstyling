<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <style>
        #addGoalButton {
            background-color: #FF0000; /* Normal red color */
            color: #FFFFFF;
            padding: 10px 20px;
            border: none;
            cursor: pointer;
        }

        #addGoalButton:disabled {
            background-color: #FF9999; /* Light red color when disabled */
            cursor: not-allowed;
        }
    </style>
    <script>
        function handleInputChange() {
            var goalInput = document.getElementById("goalInput");
            var addGoalButton = document.getElementById("addGoalButton");

            if (goalInput.value.length === 1) {
                addGoalButton.removeAttribute("disabled");
            } else {
                addGoalButton.setAttribute("disabled", true);
            }
        }
    </script>
</head>
<body>
    <label for="goalInput">Goal:</label>
    <input type="text" id="goalInput" oninput="handleInputChange()">
    <button id="addGoalButton" disabled>Add Goal</button>
</body>
</html>
