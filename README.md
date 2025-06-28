<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Free online image converter tool. Optimize, compress and convert images to various formats with quality control.">
    <meta name="keywords" content="image converter, image compression, optimize images, jpg converter, png converter, webp converter">
    <meta name="robots" content="index, follow">
    <meta name="author" content="Arunesh Prajapati">
    <title>ImageConverter Pro | Free Online Image Optimization Tool</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        :root {
            --primary: #4361ee;
            --secondary: #3f37c9;
            --accent: #4895ef;
            --light: #f8f9fa;
            --dark: #212529;
            --success: #4cc9f0;
            --warning: #f72585;
            --shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            --transition: all 0.3s ease;
        }

        body {
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            color: var(--dark);
            line-height: 1.6;
            min-height: 100vh;
            padding-bottom: 2rem;
        }

        header {
            background: linear-gradient(90deg, var(--primary), var(--secondary));
            color: white;
            padding: 1.5rem;
            text-align: center;
            box-shadow: var(--shadow);
            position: relative;
            overflow: hidden;
        }

        header::before {
            content: "";
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(255,255,255,0.1) 0%, rgba(255,255,255,0) 70%);
            transform: rotate(30deg);
        }

        .logo {
            font-size: 2.5rem;
            margin-bottom: 0.5rem;
        }

        h1 {
            font-size: 2.2rem;
            margin-bottom: 0.5rem;
        }

        .subtitle {
            font-size: 1.1rem;
            opacity: 0.9;
            max-width: 700px;
            margin: 0 auto;
        }

        .container {
            max-width: 1200px;
            margin: 2rem auto;
            padding: 0 1.5rem;
        }

        .card {
            background: white;
            border-radius: 12px;
            box-shadow: var(--shadow);
            padding: 2rem;
            margin-bottom: 2rem;
            transition: var(--transition);
        }

        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.12);
        }

        .card-title {
            color: var(--primary);
            margin-bottom: 1.5rem;
            font-size: 1.5rem;
            display: flex;
            align-items: center;
            gap: 0.75rem;
        }

        .card-title i {
            background: var(--accent);
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
        }

        .converter-section {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 2rem;
        }

        @media (max-width: 768px) {
            .converter-section {
                grid-template-columns: 1fr;
            }
        }

        .upload-area {
            border: 2px dashed var(--accent);
            border-radius: 10px;
            padding: 2rem;
            text-align: center;
            background: rgba(67, 97, 238, 0.05);
            cursor: pointer;
            transition: var(--transition);
        }

        .upload-area:hover {
            background: rgba(67, 97, 238, 0.1);
        }

        .upload-area i {
            font-size: 3rem;
            color: var(--accent);
            margin-bottom: 1rem;
        }

        .preview-container {
            text-align: center;
            padding: 1.5rem;
        }

        .preview-container h3 {
            margin-bottom: 1rem;
            color: var(--secondary);
        }

        .image-preview {
            max-width: 100%;
            max-height: 300px;
            border-radius: 8px;
            box-shadow: var(--shadow);
            margin-bottom: 1.5rem;
        }

        .controls {
            margin: 2rem 0;
        }

        .control-group {
            margin-bottom: 1.5rem;
        }

        label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 600;
            color: var(--dark);
        }

        .slider-container {
            display: flex;
            align-items: center;
            gap: 1rem;
        }

        .slider {
            flex: 1;
            -webkit-appearance: none;
            height: 8px;
            border-radius: 5px;
            background: #e0e0e0;
            outline: none;
        }

        .slider::-webkit-slider-thumb {
            -webkit-appearance: none;
            width: 20px;
            height: 20px;
            border-radius: 50%;
            background: var(--primary);
            cursor: pointer;
            transition: var(--transition);
        }

        .slider::-webkit-slider-thumb:hover {
            background: var(--secondary);
            transform: scale(1.1);
        }

        .quality-value {
            min-width: 40px;
            text-align: center;
            font-weight: bold;
            color: var(--primary);
        }

        .format-select {
            width: 100%;
            padding: 0.8rem;
            border: 2px solid #e0e0e0;
            border-radius: 8px;
            background: white;
            font-size: 1rem;
            color: var(--dark);
            transition: var(--transition);
        }

        .format-select:focus {
            border-color: var(--primary);
            outline: none;
        }

        .btn {
            display: inline-block;
            padding: 0.9rem 2rem;
            background: var(--primary);
            color: white;
            border: none;
            border-radius: 8px;
            font-size: 1rem;
            font-weight: 600;
            cursor: pointer;
            transition: var(--transition);
            text-align: center;
            width: 100%;
            margin-top: 1rem;
        }

        .btn:hover {
            background: var(--secondary);
            transform: translateY(-3px);
        }

        .btn:active {
            transform: translateY(1px);
        }

        .btn:disabled {
            background: #cccccc;
            cursor: not-allowed;
            transform: none;
        }

        .btn-download {
            background: var(--success);
            margin-top: 1.5rem;
        }

        .btn-download:hover {
            background: #3aa8d0;
        }

        .file-info {
            background: #f0f4ff;
            padding: 1rem;
            border-radius: 8px;
            margin-top: 1.5rem;
            font-size: 0.9rem;
        }

        .file-info p {
            margin: 0.3rem 0;
        }

        .ads-container {
            display: flex;
            justify-content: center;
            margin: 2rem 0;
        }

        .ad-box {
            background: white;
            border: 1px dashed #ccc;
            border-radius: 8px;
            width: 100%;
            max-width: 728px;
            height: 90px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: #888;
            font-size: 0.9rem;
            margin: 1rem 0;
        }

        .ad-label {
            text-align: center;
            font-size: 0.8rem;
            color: #666;
            margin-top: 0.5rem;
        }

        .features {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 1.5rem;
            margin-top: 2rem;
        }

        .feature {
            background: rgba(255, 255, 255, 0.7);
            border-radius: 10px;
            padding: 1.5rem;
            text-align: center;
            box-shadow: 0 2px 5px rgba(0,0,0,0.05);
            transition: var(--transition);
        }

        .feature:hover {
            transform: translateY(-5px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }

        .feature i {
            font-size: 2.5rem;
            color: var(--primary);
            margin-bottom: 1rem;
        }

        .feature h3 {
            margin-bottom: 0.75rem;
            color: var(--dark);
        }

        footer {
            text-align: center;
            padding: 2rem;
            color: #666;
            font-size: 0.9rem;
            margin-top: 2rem;
        }

        .stats {
            display: flex;
            justify-content: space-around;
            flex-wrap: wrap;
            margin: 2rem 0;
            gap: 1rem;
        }

        .stat-item {
            background: white;
            padding: 1.5rem;
            border-radius: 10px;
            min-width: 200px;
            text-align: center;
            box-shadow: var(--shadow);
        }

        .stat-number {
            font-size: 2.5rem;
            font-weight: bold;
            color: var(--primary);
            margin-bottom: 0.5rem;
        }

        .stat-label {
            color: #666;
            font-size: 1rem;
        }

        .loading {
            display: none;
            text-align: center;
            margin: 1.5rem 0;
        }

        .spinner {
            border: 4px solid rgba(0, 0, 0, 0.1);
            border-left-color: var(--primary);
            border-radius: 50%;
            width: 40px;
            height: 40px;
            animation: spin 1s linear infinite;
            margin: 0 auto;
        }

        @keyframes spin {
            to { transform: rotate(360deg); }
        }

        /* Responsive adjustments */
        @media (max-width: 768px) {
            .converter-section {
                grid-template-columns: 1fr;
            }
            
            .stats {
                flex-direction: column;
                align-items: center;
            }
            
            h1 {
                font-size: 1.8rem;
            }
            
            .subtitle {
                font-size: 1rem;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="logo">
            <i class="fas fa-image"></i>
        </div>
        <h1>ImageConverter Pro</h1>
        <p class="subtitle">Optimize and convert your images to any format with our high-quality compression tool. Reduce file size without compromising quality.</p>
    </header>

    <div class="container">
        <div class="ads-container">
            <div>
                <div class="ad-box">
                    <!-- Google AdSense Ad Unit -->
                    <script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-YOUR_AD_SENSE_ID"
                    crossorigin="anonymous"></script>
                    <!-- Ad Unit 1 -->
                    <ins class="adsbygoogle"
                         style="display:block"
                         data-ad-client="ca-pub-YOUR_AD_SENSE_ID"
                         data-ad-slot="1234567890"
                         data-ad-format="auto"
                         data-full-width-responsive="true"></ins>
                    <script>
                         (adsbygoogle = window.adsbygoogle || []).push({});
                    </script>
                </div>
                <div class="ad-label">Advertisement</div>
            </div>
        </div>

        <div class="card">
            <h2 class="card-title"><i class="fas fa-sync-alt"></i> Image Converter</h2>
            
            <div class="converter-section">
                <div class="upload-section">
                    <div class="upload-area" id="dropZone">
                        <i class="fas fa-cloud-upload-alt"></i>
                        <h3>Upload Your Image</h3>
                        <p>Drag & drop your image here or click to browse</p>
                        <input type="file" id="fileInput" accept="image/*" style="display: none;">
                    </div>
                    
                    <div class="file-info" id="fileInfo" style="display: none;">
                        <p><strong>File Name:</strong> <span id="fileName">-</span></p>
                        <p><strong>Original Size:</strong> <span id="fileSize">-</span></p>
                        <p><strong>Type:</strong> <span id="fileType">-</span></p>
                    </div>
                    
                    <div class="controls">
                        <div class="control-group">
                            <label for="quality">Compression Level</label>
                            <div class="slider-container">
                                <input type="range" min="0" max="100" value="80" class="slider" id="quality">
                                <span class="quality-value" id="qualityValue">80%</span>
                            </div>
                        </div>
                        
                        <div class="control-group">
                            <label for="format">Output Format</label>
                            <select class="format-select" id="format">
                                <option value="jpeg">JPEG</option>
                                <option value="png">PNG</option>
                                <option value="webp">WEBP</option>
                            </select>
                        </div>
                        
                        <button class="btn" id="convertBtn">Convert Image</button>
                    </div>
                </div>
                
                <div class="preview-section">
                    <div class="preview-container">
                        <h3>Converted Image Preview</h3>
                        <img id="convertedPreview" class="image-preview" alt="Converted preview">
                        
                        <div class="loading" id="loading">
                            <div class="spinner"></div>
                            <p>Processing your image...</p>
                        </div>
                        
                        <div id="resultInfo" style="display: none; margin-top: 1.5rem;">
                            <p><strong>New Size:</strong> <span id="newSize">-</span></p>
                            <p><strong>Reduction:</strong> <span id="reduction">-</span></p>
                        </div>
                        
                        <a class="btn btn-download" id="downloadBtn" style="display: none;">Download Converted Image</a>
                    </div>
                </div>
            </div>
        </div>
        
        <div class="stats">
            <div class="stat-item">
                <div class="stat-number">15,000+</div>
                <div class="stat-label">Images Converted</div>
            </div>
            <div class="stat-item">
                <div class="stat-number">97%</div>
                <div class="stat-label">Satisfied Users</div>
            </div>
            <div class="stat-item">
                <div class="stat-number">85%</div>
                <div class="stat-label">Avg. Size Reduction</div>
            </div>
        </div>
        
        <div class="card">
            <h2 class="card-title"><i class="fas fa-star"></i> Why Choose Our Tool?</h2>
            
            <div class="features">
                <div class="feature">
                    <i class="fas fa-bolt"></i>
                    <h3>Lightning Fast</h3>
                    <p>Convert images in seconds with our optimized processing engine</p>
                </div>
                
                <div class="feature">
                    <i class="fas fa-shield-alt"></i>
                    <h3>Secure & Private</h3>
                    <p>Your images are never stored or shared with third parties</p>
                </div>
                
                <div class="feature">
                    <i class="fas fa-mobile-alt"></i>
                    <h3>Fully Responsive</h3>
                    <p>Works perfectly on any device - desktop, tablet, or phone</p>
                </div>
                
                <div class="feature">
                    <i class="fas fa-crown"></i>
                    <h3>High Quality</h3>
                    <p>Maintain visual quality while reducing file size</p>
                </div>
            </div>
        </div>
        
        <div class="ads-container">
            <div>
                <div class="ad-box">
                    <!-- Google AdSense Ad Unit 2 -->
                    <script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-YOUR_AD_SENSE_ID"
                    crossorigin="anonymous"></script>
                    <!-- Ad Unit 2 -->
                    <ins class="adsbygoogle"
                         style="display:block"
                         data-ad-client="ca-pub-YOUR_AD_SENSE_ID"
                         data-ad-slot="0987654321"
                         data-ad-format="auto"
                         data-full-width-responsive="true"></ins>
                    <script>
                         (adsbygoogle = window.adsbygoogle || []).push({});
                    </script>
                </div>
                <div class="ad-label">Advertisement</div>
            </div>
        </div>
    </div>
    
    <footer>
        <p>© 2023 ImageConverter Pro. All rights reserved. | Privacy Policy | Terms of Service</p>
        <p>This tool is 100% free to use. No registration required.</p>
    </footer>

    <script>
        // DOM Elements
        const dropZone = document.getElementById('dropZone');
        const fileInput = document.getElementById('fileInput');
        const fileName = document.getElementById('fileName');
        const fileSize = document.getElementById('fileSize');
        const fileType = document.getElementById('fileType');
        const fileInfo = document.getElementById('fileInfo');
        const qualitySlider = document.getElementById('quality');
        const qualityValue = document.getElementById('qualityValue');
        const formatSelect = document.getElementById('format');
        const convertBtn = document.getElementById('convertBtn');
        const convertedPreview = document.getElementById('convertedPreview');
        const downloadBtn = document.getElementById('downloadBtn');
        const loading = document.getElementById('loading');
        const newSize = document.getElementById('newSize');
        const reduction = document.getElementById('reduction');
        const resultInfo = document.getElementById('resultInfo');
        
        let originalFile = null;
        let originalSize = 0;
        
        // Update quality value display
        qualitySlider.addEventListener('input', () => {
            qualityValue.textContent = `${qualitySlider.value}%`;
        });
        
        // File upload handling
        dropZone.addEventListener('click', () => {
            fileInput.click();
        });
        
        fileInput.addEventListener('change', (e) => {
            if (e.target.files.length > 0) {
                handleFile(e.target.files[0]);
            }
        });
        
        // Drag and drop handling
        ['dragenter', 'dragover', 'dragleave', 'drop'].forEach(eventName => {
            dropZone.addEventListener(eventName, preventDefaults, false);
        });
        
        function preventDefaults(e) {
            e.preventDefault();
            e.stopPropagation();
        }
        
        ['dragenter', 'dragover'].forEach(eventName => {
            dropZone.addEventListener(eventName, highlight, false);
        });
        
        ['dragleave', 'drop'].forEach(eventName => {
            dropZone.addEventListener(eventName, unhighlight, false);
        });
        
        function highlight() {
            dropZone.style.backgroundColor = 'rgba(67, 97, 238, 0.15)';
        }
        
        function unhighlight() {
            dropZone.style.backgroundColor = 'rgba(67, 97, 238, 0.05)';
        }
        
        dropZone.addEventListener('drop', handleDrop, false);
        
        function handleDrop(e) {
            const dt = e.dataTransfer;
            const file = dt.files[0];
            handleFile(file);
        }
        
        function handleFile(file) {
            if (!file.type.match('image.*')) {
                alert('Please select an image file (JPEG, PNG, etc.)');
                return;
            }
            
            originalFile = file;
            originalSize = file.size;
            
            // Display file info
            fileName.textContent = file.name;
            fileType.textContent = file.type.split('/')[1].toUpperCase();
            fileSize.textContent = formatFileSize(file.size);
            fileInfo.style.display = 'block';
            
            // Preview original image
            const reader = new FileReader();
            reader.onload = (e) => {
                convertedPreview.src = e.target.result;
            };
            reader.readAsDataURL(file);
            
            // Reset conversion state
            downloadBtn.style.display = 'none';
            resultInfo.style.display = 'none';
        }
        
        // Format file size for display
        function formatFileSize(bytes) {
            if (bytes === 0) return '0 Bytes';
            const k = 1024;
            const sizes = ['Bytes', 'KB', 'MB', 'GB'];
            const i = Math.floor(Math.log(bytes) / Math.log(k));
            return parseFloat((bytes / Math.pow(k, i)).toFixed(2)) + ' ' + sizes[i];
        }
        
        // Conversion function
        convertBtn.addEventListener('click', () => {
            if (!originalFile) {
                alert('Please upload an image first');
                return;
            }
            
            loading.style.display = 'block';
            downloadBtn.style.display = 'none';
            resultInfo.style.display = 'none';
            
            // Simulate processing delay
            setTimeout(() => {
                convertImage();
            }, 800);
        });
        
        function convertImage() {
            const quality = parseInt(qualitySlider.value) / 100;
            const format = formatSelect.value;
            
            const reader = new FileReader();
            reader.onload = (e) => {
                const img = new Image();
                img.onload = () => {
                    const canvas = document.createElement('canvas');
                    const ctx = canvas.getContext('2d');
                    
                    // Set canvas dimensions
                    canvas.width = img.width;
                    canvas.height = img.height;
                    
                    // Draw image on canvas
                    ctx.drawImage(img, 0, 0);
                    
                    // Convert to selected format
                    let mimeType = 'image/jpeg';
                    if (format === 'png') mimeType = 'image/png';
                    if (format === 'webp') mimeType = 'image/webp';
                    
                    // Get converted data URL
                    const dataURL = canvas.toDataURL(mimeType, quality);
                    
                    // Display converted image
                    convertedPreview.src = dataURL;
                    
                    // Calculate new file size
                    const newFileSize = Math.round((dataURL.length * 3) / 4); // Approximate base64 size
                    const sizeReduction = ((originalSize - newFileSize) / originalSize * 100).toFixed(1);
                    
                    // Display results
                    newSize.textContent = formatFileSize(newFileSize);
                    reduction.textContent = `${sizeReduction}% reduction`;
                    resultInfo.style.display = 'block';
                    
                    // Setup download
                    downloadBtn.href = dataURL;
                    downloadBtn.download = `converted-image.${format}`;
                    downloadBtn.style.display = 'block';
                    
                    // Hide loading
                    loading.style.display = 'none';
                };
                img.src = e.target.result;
            };
            reader.readAsDataURL(originalFile);
        }
        
        // Initialize AdSense ads
        document.addEventListener('DOMContentLoaded', function() {
            if (typeof adsbygoogle !== 'undefined') {
                adsbygoogle.push({});
            }
        });
    </script>
</body>
</html>
