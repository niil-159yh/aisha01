<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Image Upload & Download</title>
    <style>
        body { font-family: Arial, sans-serif; text-align: center; padding: 20px; }
        .container { margin-top: 50px; }
        button { padding: 10px 20px; margin: 10px; cursor: pointer; }
        #uploadedImage { max-width: 100%; display: none; margin-top: 20px; }
    </style>
</head>
<body>

    <h2>Upload & Download Image</h2>

    <div class="container">
        <input type="file" id="fileInput" accept="image/*">
        <button onclick="uploadImage()">Upload</button>
        <br>
        <img id="uploadedImage" alt="Uploaded Image">
        <br>
        <a id="downloadLink" style="display:none;" download="downloaded_image.png">
            <button>Download</button>
        </a>
    </div>

    <script>
        function uploadImage() {
            let fileInput = document.getElementById("fileInput");
            let uploadedImage = document.getElementById("uploadedImage");
            let downloadLink = document.getElementById("downloadLink");

            if (fileInput.files.length > 0) {
                let file = fileInput.files[0];
                let reader = new FileReader();

                reader.onload = function (e) {
                    uploadedImage.src = e.target.result;
                    uploadedImage.style.display = "block";
                    downloadLink.href = e.target.result;
                    downloadLink.style.display = "block";
                };
                reader.readAsDataURL(file);
            } else {
                alert("Please select an image to upload.");
            }
        }
    </script>

</body>
</html>
