<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Medicine Information</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
        }

        header {
            background-color: #4CAF50;
            color: white;
            text-align: center;
            padding: 15px;
            font-size: 24px;
        }

        .content {
            padding: 20px;
        }

        .medicine-list {
            margin: 20px 0;
        }

        .medicine-list li {
            cursor: pointer;
            padding: 10px;
            background-color: #e0e0e0;
            margin: 5px 0;
            border-radius: 5px;
        }

        .medicine-list li:hover {
            background-color: #c0c0c0;
        }

        .medicine-info {
            display: none;
            padding: 15px;
            background-color: #fff;
            margin: 10px 0;
            border-radius: 5px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }

        .medicine-info h3 {
            margin-top: 0;
            color: #4CAF50;
        }

        .medicine-info p {
            margin: 5px 0;
        }
    </style>
</head>
<body>

<header>
    Medicine Information System
</header>

<div class="content">
    <h2>Click on a Medicine to View Details</h2>

    <ul class="medicine-list">
        <li onclick="showInfo('paracetamol')">Paracetamol</li>
        <li onclick="showInfo('diclofenac')">Diclofenac</li>
        <li onclick="showInfo('albendazole')">Albendazole</li>
        <li onclick="showInfo('cetirizine')">Cetirizine</li>
    </ul>

    <div id="paracetamol" class="medicine-info">
        <h3>Paracetamol</h3>
        <p><strong>Purpose:</strong> Used to reduce fever and relieve mild to moderate pain.</p>
        <p><strong>Dosage:</strong> 500-1000 mg every 4-6 hours, not exceeding 4g per day.</p>
        <p><strong>Side Effects:</strong> Nausea, rash, liver damage with overdose.</p>
    </div>

    <div id="diclofenac" class="medicine-info">
        <h3>Diclofenac</h3>
        <p><strong>Purpose:</strong> Used for pain relief, inflammation, and joint disorders like arthritis.</p>
        <p><strong>Dosage:</strong> 50-100 mg twice daily with food.</p>
        <p><strong>Side Effects:</strong> Stomach upset, dizziness, risk of ulcers with prolonged use.</p>
    </div>

    <div id="albendazole" class="medicine-info">
        <h3>Albendazole</h3>
        <p><strong>Purpose:</strong> Used to treat parasitic worm infections.</p>
        <p><strong>Dosage:</strong> 400 mg as a single dose or as prescribed.</p>
        <p><strong>Side Effects:</strong> Headache, nausea, temporary hair loss.</p>
    </div>

    <div id="cetirizine" class="medicine-info">
        <h3>Cetirizine</h3>
        <p><strong>Purpose:</strong> Used to relieve allergy symptoms like runny nose and itching.</p>
        <p><strong>Dosage:</strong> 10 mg once daily for adults.</p>
        <p><strong>Side Effects:</strong> Drowsiness, dry mouth, fatigue.</p>
    </div>

</div>

<script>
    function showInfo(medicine) {
        // Hide all medicine info
        var allInfo = document.querySelectorAll('.medicine-info');
        allInfo.forEach(function(info) {
            info.style.display = 'none';
        });

        // Show the clicked medicine's info
        var selectedMedicine = document.getElementById(medicine);
        if (selectedMedicine) {
            selectedMedicine.style.display = 'block';
        }
    }
</script>

</body>
</html>
