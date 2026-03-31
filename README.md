  My Form \* { margin: 0; padding: 0; box-sizing: border-box; } body { font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; background-color: #f0ebf8; padding: 20px; min-height: 100vh; } .container { max-width: 640px; margin: 0 auto; background-color: white; border-radius: 8px; box-shadow: 0 2px 4px rgba(0,0,0,0.1); overflow: hidden; } .header { background-color: #673ab7; color: white; padding: 24px; } .header h1 { font-size: 32px; font-weight: 400; margin-bottom: 8px; } .header p { font-size: 14px; opacity: 0.9; } .form-content { padding: 24px; } .question { margin-bottom: 24px; } .question-title { font-size: 16px; font-weight: 500; color: #202124; margin-bottom: 16px; display: flex; align-items: center; } .required { color: #d93025; margin-left: 4px; } .option { display: flex; align-items: center; padding: 12px; border: 1px solid #dadce0; border-radius: 4px; margin-bottom: 8px; cursor: pointer; transition: all 0.2s; } .option:hover { background-color: #f8f9fa; } .option input\[type="radio"\] { margin-right: 12px; width: 18px; height: 18px; cursor: pointer; } .option label { cursor: pointer; flex: 1; color: #202124; } .submit-btn { background-color: #673ab7; color: white; border: none; padding: 12px 24px; font-size: 14px; font-weight: 500; border-radius: 4px; cursor: pointer; margin-top: 16px; } .submit-btn:hover { background-color: #5e35b1; box-shadow: 0 1px 3px rgba(0,0,0,0.2); } .submit-btn:disabled { background-color: #f1f3f4; color: #bdc1c6; cursor: not-allowed; } .success-message { display: none; background-color: #e6f4ea; color: #137333; padding: 16px; border-radius: 4px; margin-top: 16px; text-align: center; } .error-message { display: none; background-color: #fce8e6; color: #c5221f; padding: 16px; border-radius: 4px; margin-top: 16px; } .footer { padding: 24px; text-align: right; color: #5f6368; font-size: 12px; }

My Form
=======

Your response helps us improve

What is your favorite option? \*

 Option 1

 Option 2

 Option 3

 Option 4

 Other

Submit

✓ Thank you! Your response has been recorded.

✕ Please select an option before submitting.

Not a Google Form

const form = document.getElementById('myForm'); const successMessage = document.getElementById('successMessage'); const errorMessage = document.getElementById('errorMessage'); form.addEventListener('submit', function(e) { e.preventDefault(); // Hide any previous messages successMessage.style.display = 'none'; errorMessage.style.display = 'none'; // Get selected value const selected = document.querySelector('input\[name="selection"\]:checked'); if (!selected) { errorMessage.style.display = 'block'; return; } // For now, just show success message // To use Formspree, replace this section with Formspree integration successMessage.style.display = 'block'; form.reset(); // After 3 seconds, hide the success message setTimeout(() => { successMessage.style.display = 'none'; }, 3000); });
