# Secure Image Steganography Tool with Password Authentication

##  Project Definition: What is this project and what does it do?
This security utility is an **Image Steganography Application** developed using Python and **OpenCV**. It allows a user to inject or embed hidden text data strings directly into the individual RGB pixel blocks of an image carrier and extract the payload securely via custom passcode authentication layers.

### Why is this used? / How does it help?
1. **Hidden Communication (Covert Channels):** It secures data in transit by hiding secret messages inside standard image files (`encryptedImage.jpg`), preventing unauthorized network sniffers or interceptors from noticing that raw text data is being sent.
2. **Pixel-Level Cryptographic Array Mapping:** Instead of simply appending text files at the end of a binary string, it steps through visual color channel array indexes (`Blue, Green, Red matrices`) to hide characters dynamically.
3. **Basic Access Control Authentication:** It builds a data validation gate matching variable text passcodes. If an unauthorized entity provides an invalid password string, the application denies data decryption rights (`YOU ARE NOT auth`).

### Core Technical Workflow / Architecture
*   **Encoding Phase (Data Injection):** Translates every string text character payload into custom integer codes using internal ASCII dictionary parameters (`chr(i) <-> i`), sequentially mapping pixel layer bounds `img[n, m, z]` across three core color metrics channels.
*   **Decoding Phase (Extraction Loop):** Reads the exact sequential matrix steps inside image coordinates arrays, systematically translating multi-dimensional color integers back to standard string assets upon verification.

###  Prerequisites & Tool Stack
*   **Language Environment:** Python 3.x Engine
*   **Libraries Implemented:** `opencv-python` (`cv2` for spatial image modifications), `os` (for native system processes execution logic).
