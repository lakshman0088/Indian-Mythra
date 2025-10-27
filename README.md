# Indian-Mythra
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Indian Mythra Railway Booking System</title>
    <style>
        :root {
            --primary-color: #2c3e50;
            --secondary-color: #e74c3c;
            --accent-color: #3498db;
            --background-color: #ecf0f1;
            --text-color: #2c3e50;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: var(--background-color);
            color: var(--text-color);
            line-height: 1.6;
        }

        header {
            background-color: var(--primary-color);
            color: white;
            padding: 2rem;
            text-align: center;
        }

        #timer {
            margin-top: 1rem;
            font-size: 1.2rem;
            color: var(--secondary-color);
        }

        main {
            max-width: 1200px;
            margin: 2rem auto;
            padding: 0 1rem;
        }

        .train-list {
            margin-bottom: 3rem;
        }

        .train-card {
            background: white;
            border-radius: 8px;
            padding: 1.5rem;
            margin-bottom: 1rem;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }

        .train-details ul {
            list-style: none;
            margin: 1rem 0;
        }

        .reserve-btn, .payment-btn {
            background-color: var(--accent-color);
            color: white;
            border: none;
            padding: 0.8rem 1.5rem;
            border-radius: 4px;
            cursor: pointer;
            transition: background-color 0.3s;
        }

        .reserve-btn:hover, .payment-btn:hover {
            background-color: #2980b9;
        }

        .booking-form {
            background: white;
            padding: 2rem;
            border-radius: 8px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: bold;
        }

        input[type="text"],
        textarea,
        select {
            width: 100%;
            padding: 0.8rem;
            border: 1px solid #ddd;
            border-radius: 4px;
            font-size: 1rem;
        }

        textarea {
            height: 100px;
            resize: vertical;
        }

        .cancellation-policy {
            background: #fff3f3;
            padding: 1rem;
            border-radius: 8px;
            margin-top: 2rem;
            border-left: 4px solid var(--secondary-color);
        }

        @media (max-width: 768px) {
            .train-card {
                padding: 1rem;
            }

            .booking-form {
                padding: 1rem;
            }
        }
    </style>
</head>
<body>
    <header>
        <h1>Indian Mythra Railway Booking System</h1>
        <p id="timer">Booking opens at - AC: 11:00 AM | Non-AC: 10:30 AM</p>
    </header>

    <main>
        <!-- Available Trains Section -->
        <section class="train-list">
            <h2>Available Trains</h2>
            <div class="train-container" id="trainList">
                <div class="train-card">
                    <h3>Train #12345 - Express</h3>
                    <div class="train-details">
                        <p>Available Seats:</p>
                        <ul>
                            <li>AC Coaches: 3 (72 seats)</li>
                            <li>Non-AC Coaches: 5 (90 seats)</li>
                            <li>Available Berths: Upper - 24, Lower - 20, Middle - 28</li>
                        </ul>
                    </div>
                    <button class="reserve-btn">Reserve Seat</button>
                </div>
            </div>
        </section>

        <!-- Passenger Booking Form -->
        <section class="booking-form" id="bookingForm">
            <h2>Passenger Details</h2>
            <form>
                <div class="form-group">
                    <label for="name">Full Name:</label>
                    <input type="text" id="name" required>
                </div>

                <div class="form-group">
                    <label for="address">Address:</label>
                    <textarea id="address" required></textarea>
                </div>

                <div class="form-group">
                    <label for="pickup">Pickup Point:</label>
                    <input type="text" id="pickup" required>
                </div>

                <div class="form-group">
                    <label for="destination">Destination:</label>
                    <input type="text" id="destination" required>
                </div>

                <div class="form-group">
                    <label for="coach">Select Coach Type:</label>
                    <select id="coach" required>
                        <option value="">Select Coach</option>
                        <option value="ac">AC Coach</option>
                        <option value="nonac">Non-AC Coach</option>
                    </select>
                </div>

                <div class="form-group">
                    <label for="berth">Berth Preference:</label>
                    <select id="berth" required>
                        <option value="">Select Berth</option>
                        <option value="upper">Upper</option>
                        <option value="middle">Middle</option>
                        <option value="lower">Lower</option>
                    </select>
                </div>

                <div class="form-group">
                    <label>Upload Photo:</label>
                    <input type="file" accept="image/*" required>
                </div>

                <button type="submit" class="payment-btn">Proceed to Payment</button>
            </form>
        </section>

        <!-- Cancellation Info -->
        <section class="cancellation-policy">
            <h2>Cancellation Policy</h2>
            <p>Note: Only 25% of the ticket fare will be refunded upon cancellation.</p>
        </section>
    </main>
</body>
</html>
