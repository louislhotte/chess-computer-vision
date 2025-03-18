# Chess Computer Vision Project

<div align="center">
  <img src="https://images.chesscomfiles.com/uploads/v1/blog/291978.0ba48c8e.5000x5000o.b1dd3c4ba347.png" alt="Chess.com Logo" width="200">
  <img src="https://www.regencychess.co.uk/images/how-to-set-up-a-chessboard/how-to-set-up-a-chessboard-7.jpg" alt="Chess Board" width="200">
</div>


## Objective
Develop a computer vision system capable of recognizing a chessboard, detecting pieces, and tracking moves from an image or a video stream. The project will utilize OpenCV and machine learning techniques to identify and reconstruct a chess game.

This project is being developed as part of my CentraleSupélec Computer Vision coursework.

## Scope
- **Input:** Chessboard image or video feed.
- **Output:** FEN (Forsyth–Edwards Notation) or move list.

### Constraints:
- Fixed camera angle (top-down view preferred).
- Standard chess pieces.
- Standard board (8x8 grid, alternating colors).

## Methodology
The approach follows the methodology described in the article **"Computer Vision System for Chess Game Reconstruction"** by M. Piškorec et al.

### Step-by-step Process
1. **Image Preprocessing:**
   - Convert image to grayscale.
   - Apply noise reduction techniques (Gaussian blur, adaptive thresholding).
2. **Board and Piece Detection:**
   - Identify the chessboard grid using corner detection techniques (e.g., OpenCV’s `cvFindChessboardCorners`).
   - Segment the chessboard into individual squares.
   - Detect the presence of pieces using feature extraction methods.
3. **Move Detection:**
   - Compare consecutive frames to detect changes.
   - Identify start and end positions of the moved pieces.
   - Convert detected moves into standard chess notation.
4. **Piece Classification:**
   - Use Support Vector Machine (SVM) classifiers for identifying different chess pieces based on their shape.
   - Train the classifier using a dataset of labeled chess pieces.
5. **Game Reconstruction:**
   - Track moves and construct a move list.
   - Generate Forsyth–Edwards Notation (FEN) for board state representation.

## Technologies Used
- **Programming Language:** Python (OpenCV, NumPy, TensorFlow/Keras for machine learning models)
- **Computer Vision:** OpenCV (for board and piece recognition)
- **Machine Learning:** SVM (Support Vector Machine) for classification OR dino-v2 for better performances
- **Data Formats:** FEN notation for chess state representation (or a list?)

## Reference
Piškorec, M., Antulov-Fantulin, N., Ćurić, J., Dragoljević, O., Ivanac, V., & Karlović, L. (2010). **Computer Vision System for the Chess Game Reconstruction.** Faculty of Electrical Engineering and Computing, University of Zagreb.

## Future Enhancements
- Implement Deep Learning (CNN) for improved piece classification.
- Add support for real-time tracking with webcam input.
- Enhance robustness against varying lighting conditions and occlusions.

## License
This project is open-source and available under the MIT License.

---

### Contributors
- **[Louis Lhotte]**
- **[Paul-Alexandre Marenghi]**

For any queries or contributions, feel free to open an issue or submit a pull request!
