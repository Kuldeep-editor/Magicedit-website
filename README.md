Here is your photo editor website HTML code. You can copy this into a file and save it as index.html:

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>MagicEdit - Photo & Video Editor</title>
  <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
</head>
<body class="bg-gray-100 text-gray-800">
  <header class="bg-blue-600 text-white p-4">
    <h1 class="text-3xl font-bold">MagicEdit</h1>
    <p class="text-sm">Edit your photos & videos with magical effects</p>
  </header>

  <section class="p-6">
    <h2 class="text-2xl font-semibold mb-4">Features</h2>
    <ul class="list-disc pl-6 space-y-2">
      <li>Reduce Blur</li>
      <li>Crop</li>
      <li>Rotate</li>
      <li>Remove Background</li>
      <li>Add Frames</li>
      <li>Style Transform: Ghibli, Disney, Pixar, Sketch, and more</li>
    </ul>
  </section>

  <section class="p-6 bg-white mt-4 rounded shadow">
    <h2 class="text-xl font-semibold mb-2">Upload Your Media</h2>
    <form id="upload-form" enctype="multipart/form-data">
      <input type="file" name="file" accept="image/*,video/*" class="mb-4" required />
      <select name="operation" class="block mb-4 p-2 border rounded">
        <option value="blur">Reduce Blur</option>
        <option value="crop">Crop</option>
        <option value="rotate">Rotate</option>
        <option value="remove_bg">Remove Background</option>
        <option value="frame">Add Frame</option>
        <option value="style_ghibli">Style: Ghibli</option>
        <option value="style_disney">Style: Disney</option>
        <option value="style_pixar">Style: Pixar</option>
        <option value="style_sketch">Style: Sketch</option>
      </select>
      <button type="submit" class="bg-blue-500 hover:bg-blue-600 text-white px-4 py-2 rounded">Edit Now</button>
    </form>
    <div id="result" class="mt-4 hidden">
      <h3 class="text-lg font-medium">Your edited media will appear below:</h3>
      <img id="preview" src="" alt="Edited media" class="mt-2 max-w-full" />
    </div>
  </section>

  <section class="p-6 mt-4">
    <h2 class="text-xl font-semibold mb-2">Pricing</h2>
    <p>Free: 5 edits per day</p>
    <p>Premium: ₹30/month for unlimited access</p>
    <button class="bg-green-500 hover:bg-green-600 text-white px-4 py-2 rounded mt-2">Get Premium</button>
  </section>

  <footer class="bg-blue-600 text-white p-4 mt-6 text-center">
    <p>&copy; 2025 MagicEdit. All rights reserved.</p>
  </footer>

  <script>
    const form = document.getElementById('upload-form');
    const result = document.getElementById('result');
    const preview = document.getElementById('preview');

    form.addEventListener('submit', async (e) => {
      e.preventDefault();
      const formData = new FormData(form);

      const res = await fetch('https://your-backend-api.com/process', {
        method: 'POST',
        body: formData,
      });

      const data = await res.json();
      preview.src = data.output_url;
      result.classList.remove('hidden');
    });
  </script>
</body>
</html>


---

To Use It:

1. Open any code editor (like Notepad or VS Code).


2. Paste the code above into a new file.


3. Save it as index.html.


4. Double-click to open in your browser.



Let me know if you'd like this as a ZIP file, or if you want help uploading it online!

