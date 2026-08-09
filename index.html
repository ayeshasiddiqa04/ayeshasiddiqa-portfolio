const year = document.getElementById('year');
if (year) {
  year.textContent = new Date().getFullYear();
}

const filterButtons = document.querySelectorAll('.filter-btn');
const projectCards = document.querySelectorAll('.project-card');

filterButtons.forEach((button) => {
  button.addEventListener('click', () => {
    filterButtons.forEach((btn) => btn.classList.remove('active'));
    button.classList.add('active');

    const filter = button.dataset.filter;

    projectCards.forEach((card) => {
      const matches = filter === 'all' || card.dataset.category === filter;
      card.classList.toggle('hidden', !matches);
    });
  });
});

const form = document.getElementById('contactForm');
const status = document.getElementById('formStatus');

if (form) {
  form.addEventListener('submit', async (event) => {
    event.preventDefault();

    const formData = new FormData(form);
    const name = (formData.get('name') || '').toString().trim();
    const email = (formData.get('email') || '').toString().trim();
    const message = (formData.get('message') || '').toString().trim();

    if (!name || !email || !message) {
      status.textContent = 'Please fill out all fields before sending your message.';
      status.style.color = '#ffc857';
      return;
    }

    const payload = {
      name,
      email,
      message,
      _subject: `New portfolio enquiry from ${name}`
    };

    status.textContent = 'Sending your message...';
    status.style.color = '#5eead4';

    const emailAddress = 'hello@ayeshasiddiqa.dev';

    try {
      const response = await fetch(`https://formsubmit.co/ajax/${emailAddress}`, {
        method: 'POST',
        headers: {
          'Content-Type': 'application/json',
          Accept: 'application/json'
        },
        body: JSON.stringify(payload)
      });

      if (response.ok) {
        form.reset();
        status.textContent = 'Your message has been sent successfully. Thank you!';
        status.style.color = '#5eead4';
        return;
      }

      throw new Error('Form service rejected the request');
    } catch (error) {
      const mailtoLink = `mailto:${emailAddress}?subject=${encodeURIComponent(`Portfolio enquiry from ${name}`)}&body=${encodeURIComponent(`Name: ${name}\nEmail: ${email}\n\nMessage:\n${message}`)}`;
      window.location.href = mailtoLink;
      status.textContent = 'Your email app is opening. Please send the message to continue.';
      status.style.color = '#ffc857';
      form.reset();
    }
  });
}
