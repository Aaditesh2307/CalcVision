# AI Calculator

An interactive application that uses AI to recognize and solve handwritten mathematical expressions. Draw a math problem on the canvas and let the AI calculate the answer for you.

## Overview

The AI Calculator consists of two main components:

- **Frontend (calc-fe)**: A React-based web interface that allows users to draw mathematical expressions on a canvas.
- **Backend (calc-be)**: A FastAPI server that processes the drawn images using Google's Gemini API to recognize and solve mathematical expressions.

## Features

- Draw mathematical expressions using a digital canvas
- Multiple color options for drawing
- Real-time interpretation of handwritten math
- Support for various types of calculations:
  - Basic arithmetic (addition, subtraction, multiplication, division)
  - Equations and variable assignments
  - Algebraic expressions
  - Graphical math problems
  - Abstract concept interpretation
- Variable storage: assigned variables are remembered for future calculations
- Draggable LaTeX-rendered results display

## Technology Stack

### Frontend (calc-fe)

- React 18 with TypeScript
- Vite for build and development
- TailwindCSS for styling
- MathJax for LaTeX rendering
- HTML5 Canvas for drawing capabilities
- Mantine UI components
- React Router for navigation
- Axios for API requests

### Backend (calc-be)

- FastAPI framework
- Google Gemini 1.5 Flash API for AI image recognition
- Pillow for image processing
- Python 3.x
- Pydantic for data validation

## Getting Started

### Prerequisites

- Node.js (v16+)
- Python 3.8+
- Google Gemini API key

### Frontend Setup

1. Clone the repository
2. Navigate to the frontend directory:
   ```
   cd calc-fe
   ```
3. Install dependencies:
   ```
   npm install
   ```
4. Start the development server:
   ```
   npm run dev
   ```

### Backend Setup

1. Navigate to the backend directory:
   ```
   cd calc-be
   ```
2. Install the required packages:
   ```
   pip install -r requirements.txt
   ```
3. Add your Google Gemini API key to the constants.py file or as an environment variable
4. Start the server:
   ```
   python main.py
   ```

## Usage

1. Open the application in your browser (default: http://localhost:5173)
2. Use the canvas to draw a mathematical expression
3. Select a color from the color palette if needed
4. Click the "Run" button to process the expression
5. View the result displayed as LaTeX on the screen
6. Drag the result to position it where you want
7. Click "Reset" to clear the canvas and start again

## Supported Mathematical Operations

The application can recognize and solve:

- Basic arithmetic operations (+, -, \*, /)
- Variable assignments (x = 5)
- Equations (x² + 2x + 1 = 0)
- Multiple variable systems
- Mathematical word problems (drawn graphically)
- Complex expressions using PEMDAS rules

## System Architecture

The system works as follows:

1. User draws a mathematical expression on the frontend canvas
2. Canvas image is converted to base64 and sent to the backend
3. Backend processes the image using the Gemini API
4. Response is parsed and processed into structured data
5. Results are sent back to the frontend
6. Frontend renders the results using LaTeX and MathJax

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- Google Gemini API for AI image processing
- MathJax for mathematical typesetting
- React community for the extensive component ecosystem
