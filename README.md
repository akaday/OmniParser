# OmniParser: Screen Parsing tool for Pure Vision Based GUI Agent

<p align="center">
  <img src="imgs/logo.png" alt="Logo">
</p>

[![arXiv](https://img.shields.io/badge/Paper-green)](https://arxiv.org/abs/2408.00203)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

📢 [[Project Page](https://microsoft.github.io/OmniParser/)] [[Blog Post](https://www.microsoft.com/en-us/research/articles/omniparser-for-pure-vision-based-gui-agent/)] [[Models](https://huggingface.co/microsoft/OmniParser)] 

**OmniParser** is a comprehensive method for parsing user interface screenshots into structured and easy-to-understand elements, which significantly enhances the ability of GPT-4V to generate actions that can be accurately grounded in the corresponding regions of the interface. 

## News
- [2024/10] Both Interactive Region Detection Model and Icon functional description model are released! [Hugginface models](https://huggingface.co/microsoft/OmniParser)
- [2024/09] OmniParser achieves the best performance on [Windows Agent Arena](https://microsoft.github.io/WindowsAgentArena/)! 

## Install 
Install environment:
```python
conda create -n "omni" python==3.12
conda activate omni
pip install -r requirements.txt
```

Then download the model ckpts files in: https://huggingface.co/microsoft/OmniParser, and put them under weights/, default folder structure is: weights/icon_detect, weights/icon_caption_florence, weights/icon_caption_blip2. 

Finally, convert the safetensor to .pt file. 
```python
python weights/convert_safetensor_to_pt.py
```

## Examples:
We put together a few simple examples in the demo.ipynb. 

## Gradio Demo
To run gradio demo, simply run:
```python
python gradio_demo.py
```

## Running demo.ipynb
To run the cells in `demo.ipynb` and verify everything is working as expected, follow these steps:

1. Open the `demo.ipynb` file in Jupyter Notebook or JupyterLab.
2. Run each cell sequentially by clicking on the "Run" button or pressing `Shift + Enter`.
3. Verify the output of each cell to ensure it matches the expected results.

## Debugging Jupyter Notebooks
To debug Jupyter notebooks effectively, you can use the following tools and techniques:

1. **Built-in Debugging Tools**:
   - Use the `%debug` magic command to enter the interactive debugger.
   - Use the `print` function to display variable values and track the flow of execution.
   - Leverage the `pdb` module to set breakpoints and step through the code.

2. **Organize and Structure Your Code**:
   - Break down your code into smaller, manageable cells to isolate issues more easily.
   - Use comments and markdown cells to document your code and explain the logic.
   - Ensure that each cell performs a specific task and avoid having too much code in a single cell.

3. **Use External Tools and Libraries**:
   - Use external libraries like `ipdb` for an enhanced debugging experience.
   - Leverage visualization libraries like `matplotlib` or `seaborn` to plot data and identify issues visually.
   - Utilize tools like `nbdime` to compare and merge notebook files, which can help identify changes that introduced bugs.

## Verifying Functionality
After running the cells in `demo.ipynb`, you can verify if everything is working as expected by checking the following:

1. Ensure that the outputs of the cells match the expected results.
2. Check for any error messages or warnings in the notebook.
3. Verify that the functionality demonstrated in the notebook aligns with the intended behavior of the repository.

## 📚 Citation
Our technical report can be found [here](https://arxiv.org/abs/2408.00203).
If you find our work useful, please consider citing our work:
```
@misc{lu2024omniparserpurevisionbased,
      title={OmniParser for Pure Vision Based GUI Agent}, 
      author={Yadong Lu and Jianwei Yang and Yelong Shen and Ahmed Awadallah},
      year={2024},
      eprint={2408.00203},
      archivePrefix={arXiv},
      primaryClass={cs.CV},
      url={https://arxiv.org/abs/2408.00203}, 
}
```
