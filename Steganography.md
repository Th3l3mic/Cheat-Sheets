<h1>Steganography cheat sheet for CTFs:</h1>
--------------------------------------------------------------------------------------------------------------------------------------------

<b>Steganography is the practice of concealing a file, message, image, or video within another file, message, image, or video.</b>
<p></p>
<p></p>
1. Identify hidden data in images:
- Use tools like steghide, StegSolve, and ExifTool to extract hidden data from images.
- Look for discrepancies in file sizes, metadata, and visual inspection of the image.
<h3>Examples:</h3>
<code>steghide extract -sf file.jpg</code>
<p></p>
<b>StegSolve</b>
<p></p>
<code>wget https://github.com/eugenekolo/sec-tools/raw/master/stego/stegsolve/stegsolve/stegsolve.jar
java -jar stegsolve.jar</code>
<p></p>
<b>Exiftool</b>
<p></p>
<code>exiftool file.jpg</code>
<p></p>
2. Identify hidden data in audio files:
- Use tools like Sonic Visualizer and Audacity to analyze audio files for hidden data.
- Look for anomalies in spectrograms or waveforms that indicate hidden data.
<p></p>

3. Identify hidden data in text files:
- Use tools like strings and grep to search for hidden data in text files (sometimes also works on different filetypes).
- Look for patterns or anomalies in the text that may indicate hidden data.

4. Brute force password attacks:
- If a password is required to extract hidden data, use a brute force attack with tools like John the Ripper or Hashcat to crack the password.
- Use stegcracker for bruteforce hidden files:
- <p></p>
  <code> stegcracker file wordlist</code>
  <p></p>
5. Use online tools and websites:
- Utilize online steganography tools like CyberChef, StegoSuite, and Stegdetect to analyze and extract hidden data.

6. Experiment with different techniques:
- Try different steganography techniques such as LSB (Least Significant Bit) encoding, DCT (Discrete Cosine Transform) encoding, and F5 algorithm to extract hidden data.

  T.
