<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Ilia Built Coaching - Online Training Programs</title>
  <style>
    :root {
      --primary: #1e1e2f;
      --accent:  #4e5d94;
      --light:   #f4f4f9;
      --text:    #333;
      --white:   #fff;
    }
    * { box-sizing: border-box; margin: 0; padding: 0; }
    body { 
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      color: var(--text);
      background: var(--light);
    }
    header { 
      background: var(--primary);
      color: var(--white);
      text-align: center;
      padding: 3rem 1rem;
    }
    header h1 { font-size: 2.75rem; letter-spacing: 1px; }
    header p  { font-size: 1.25rem; margin-top: 0.5rem; }

    /* Enhanced About Section */
    #readme {
      background: var(--white);
      padding: 2.5rem 1rem;
      text-align: center;
      border-left: 6px solid var(--accent);
      box-shadow: 0 4px 10px rgba(0,0,0,0.05);
      margin: 2rem 1rem;
    }
    #readme h2 { 
      font-size: 2.2rem;
      color: var(--primary);
      margin-bottom: 0.75rem;
      letter-spacing: 1px;
    }
    #readme p {
      max-width: 700px;
      margin: 1rem auto;
      font-size: 1.15rem;
      line-height: 1.6;
      font-style: italic;
      color: #444;
    }

    #programs {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 2rem;
      padding: 4rem 1rem;
    }
    .program {
      background: var(--white);
      border-radius: 12px;
      width: 320px;
      padding: 2rem;
      box-shadow: 0 6px 15px rgba(0,0,0,0.1);
      text-align: center;
      transition: transform 0.3s;
    }
    .program:hover { transform: translateY(-8px); }
    .program h2 { 
      font-size: 1.75rem;
      color: var(--primary);
      margin-bottom: 0.5rem;
    }
    .program p.price {
      font-size: 1.5rem;
      font-weight: bold;
      margin: 0.75rem 0;
    }
    .program ul {
      list-style: none;
      text-align: left;
      margin: 1rem 0;
    }
    .program ul li {
      margin-bottom: 0.75rem;
      padding-left: 1.2rem;
      position: relative;
    }
    .program ul li::before {
      content: '✔';
      position: absolute;
      left: 0;
      color: var(--accent);
    }
    .program button {
      background: var(--accent);
      color: var(--white);
      border: none;
      padding: 0.75rem 1.5rem;
      border-radius: 6px;
      cursor: pointer;
      font-size: 1rem;
      margin-top: 1rem;
    }
    .program button:hover { background: #3b4a7a; }

    /* Contact section hidden by default */
    #contact {
      display: none;
      text-align: center;
      padding: 3rem 1rem;
      background: var(--white);
      border-top: 4px solid var(--accent);
    }
    #contact.active { display: block; }
    #contact h2 {
      font-size: 2rem;
      color: var(--primary);
      margin-bottom: 1rem;
    }
    #contact form {
      max-width: 400px;
      margin: 0 auto;
      text-align: left;
    }
    #contact label {
      display: block;
      margin-bottom: 0.5rem;
      font-weight: bold;
    }
    #contact input,
    #contact textarea {
      width: 100%;
      padding: 0.75rem;
      margin-bottom: 1rem;
      border: 1px solid #ccc;
      border-radius: 6px;
      font-size: 1rem;
    }
    #contact button {
      background: var(--primary);
      color: var(--white);
      border: none;
      padding: 0.75rem 1.5rem;
      border-radius: 6px;
      cursor: pointer;
      width: 100%;
      font-size: 1rem;
    }
    #contact p.info {
      margin-top: 1rem;
      font-size: 1rem;
    }
    .important {
      color: red;
      font-weight: bold;
      margin-top: 0.5rem;
    }

    footer {
      text-align: center;
      padding: 1rem;
      background: var(--primary);
      color: var(--white);
      font-size: 0.9rem;
    }

    @media (max-width: 640px) {
      #programs { flex-direction: column; align-items: center; }
    }
  </style>
</head>
<body>
  <header>
    <h1>Ilia Built Coaching</h1>
    <p>Transform Your Body, Transform Your Life</p>
  </header>

  <section id="readme">
    <h2>About Ilia Nazari</h2>
    <p>Hi, I’m Ilia Nazari—an ISSA-certified personal trainer with CPR & AED certifications and an IKF Don 2 black belt in kickboxing. With years of hands-on coaching experience, I combine evidence-based training techniques and combat discipline to push you beyond your limits. My mission is to help you escape average, redefine your potential, and embrace a stronger, healthier you. Ready to break free from the ordinary?</p>
  </section>

  <section id="programs">
    <div class="program">
      <h2>Elite Training Program</h2>
      <p class="price">8 Weeks — $80</p>
      <ul>
        <li>24/7 Support</li>
        <li>Regular Progress Checks</li>
        <li>Custom Workout Plan</li>
        <li>Nutrition Guidance</li>
      </ul>
      <button onclick="showForm('Elite')">Sign Up Now</button>
    </div>
    <div class="program">
      <h2>Basic Training Program</h2>
      <p class="price">4 Weeks — $50</p>
      <ul>
        <li>Customized Training Program</li>
      </ul>
      <button onclick="showForm('Basic')">Sign Up Now</button>
    </div>
    <div class="program">
      <h2>1-on-1 Coaching (In Person)</h2>
      <p class="price">$50 per session</p>
      <ul>
        <li>Personalized Workout Sessions</li>
        <li>Form and Technique Guidance</li>
        <li>Flexible Scheduling</li>
      </ul>
      <button onclick="showForm('1-on-1 Coaching')">Sign Up Now</button>
    </div>
  </section>

  <section id="contact">
    <h2>Sign Up</h2>
    <form id="signupForm">
      <label for="programType">Program</label>
      <input type="text" id="programType" name="programType" readonly>

      <label for="name">Your Full Name</label>
      <input type="text" id="name" name="name" placeholder="Enter your full name" required>

      <label for="phone">Phone Number (for e-Transfer)</label>
      <input type="tel" id="phone" name="phone" placeholder="e.g. 4165551234" pattern="[0-9]{10}" required>

      <label for="goals">Your Goals</label>
      <textarea id="goals" name="goals" rows="4" placeholder="Tell me your main goals" required></textarea>

      <button type="submit">Submit</button>
    </form>
    <p class="info">After submitting, please e-transfer your program fee to <strong>ilia.nazari2023@gmail.com</strong>.</p>
    <p class="important">Important: Include your full name and phone number in the message when sending the e-Transfer.</p>
  </section>

  <footer>
    <p>© 2025 Ilia Built Coaching</p>
  </footer>

  <script>
    async function showForm(type) {
      document.getElementById('signupForm').reset();
      document.getElementById('programType').value = type;
      document.getElementById('contact').classList.add('active');
      window.scrollTo({ top: document.getElementById('contact').offsetTop, behavior: 'smooth' });
    }

    document.getElementById('signupForm').addEventListener('submit', async function(e) {
      e.preventDefault();
      const programType = document.getElementById('programType').value;
      const name = document.getElementById('name').value;
      const phone = document.getElementById('phone').value;
      const goals = document.getElementById('goals').value;

      try {
        await fetch('https://your-backend.example.com/sendEmail', {
          method: 'POST',
          headers: { 'Content-Type': 'application/json' },
          body: JSON.stringify({
            to: 'ilia.nazari2023@gmail.com',
            subject: `New Signup: ${programType}`,
            programType,
            name,
            phone,
            goals
          })
        });
      } catch (err) {
        console.error('Email send failed', err);
      }

      alert(`Thanks, ${name}! We’ll be in touch soon about your ${programType} program.`);
      this.reset();
      document.getElementById('contact').classList.remove('active');
    });
  </script>
</body>
</html>
