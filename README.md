# Morphing 3D Foot Model in Blender

## Overview
This project focuses on morphing a 3D foot model in Blender based on specific input values using shape keys. The methodology involves dividing the foot into proportions, marking specific areas using vertex groups, and adjusting the model using shape keys for precise modifications. The goal is to create accurate, scalable, and realistic foot models for applications such as medical research, fashion, and ergonomic design.

## Features
- **Vertex Group Marking**: Identifies specific areas of the foot model for precise scaling and morphing.
- **Shape Key Morphing**: Adjusts the foot dimensions dynamically based on input parameters.
- **Automated Scaling & Transformation**: Ensures proportional adjustments without compromising model realism.
- **Customizable Parameters**: Users can define foot measurements (A to I) for model adjustments.
- **Python Scripting for Blender**: Automates the process using Blender's Python API.

## Installation
1. Ensure you have **Blender 4.1** installed on your system.
2. Clone this repository:
   ```sh
   git clone https://github.com/your-repo-name.git
   cd your-repo-name
   ```
3. Open Blender and enable scripting.
4. Load the `morphing_Left.py` script into the Blender scripting editor.

## Usage
1. Load your 3D foot model (`.blend` file) into Blender.
2. Run the script to initialize the vertex groups and shape keys.
3. Provide input measurements for foot dimensions:
   ```python
   old_size_dict = {
       'A': 23.716, 'B': 20.034, 'C': 8.033, 'D': 16.944, 'E': 15.366,
       'F': 9.617, 'G': 5.237, 'H': 4, 'I': 10.017
   }
   new_size_dict = {
       'A': 22.392, 'B': 19.128, 'C': 7.393, 'D': 16.359, 'E': 14.231,
       'F': 9.414, 'G': 5.696, 'H': 4.13, 'I': 9.564
   }
   morphing_keys = ['A', 'B', 'D', 'E', 'I']
   morphing_sole('FootModel', old_size_dict, new_size_dict, morphing_keys)
   ```
4. The model will automatically morph based on the provided values.
5. Adjust and fine-tune the shape keys manually if necessary.

## Methodology
### 1. **Divide the Foot into Proportions**
   - Use bisection tools to create specific foot proportions.
   - Mark specific areas using vertex groups.
### 2. **Adjust the Model Using Shape Keys**
   - Utilize shape keys to scale and morph the 3D foot model according to the defined proportions.
   - Sequentially morph the model starting from the toes and moving to the heel.
### 3. **Final Adjustments & Refinement**
   - Validate the model dimensions using RMSE (Root Mean Square Error) calculations.
   - Ensure accurate scaling by refining vertex group selection.

## Experiment Results & Findings
- **Initial Challenges**: Proportional editing complications led to unrealistic results.
- **Revised Approach**: Implemented sequential morphing and refined shape key application.
- **Accuracy Evaluation**: RMSE calculations showed improvements in model precision.
- **Future Improvements**:
  - Enhance vertex group selection for more accurate deformations.
  - Explore alternative morphing methods such as Armature-based transformations.
  - Integrate automated weight painting for better shape retention.

## Contributors
- **Anecha Prasobvittaya**
- Tanadhon Dumnernpan
- Suppakorn Pojsomphong
- Patiparn Tangmongkolpaisan
- Wongpan Wongmethakul

## License
This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.

## Acknowledgments
This project was developed as part of a research experiment at Mahidol University, Faculty of Information and Communication Technology, 2023.

