# PDF Website  

This is a simple website where users can view and download PDFs.  

## Features  
- Upload and share PDFs  
- View PDFs online  
- Simple and user-friendly design  

## Live Website  
[Click here to visit](https://your-username.github.io/pdf-website/)  
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Create PDF</title>
</head>
<body>
    <h1>Create a PDF</h1>
    <textarea id="text" placeholder="Enter your text"></textarea>
    <button onclick="generatePDF()">Download PDF</button>

    <script src="https://cdnjs.cloudflare.com/ajax/libs/jspdf/2.5.1/jspdf.umd.min.js"></script>
    <script>
        const { jsPDF } = window.jspdf;
        
        function generatePDF() {
            const pdf = new jsPDF();
            pdf.text(document.getElementById('text').value, 10, 10);
            pdf.save('document.pdf');
        }
    </script>
</body>
</html>
