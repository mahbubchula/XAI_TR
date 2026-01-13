# Examples Directory

Welcome to the examples section of the XAI_TR course! This directory contains practical code samples, Jupyter notebooks, and datasets to help you learn by doing.

## 📁 Directory Structure

```
examples/
├── datasets/          # Sample datasets for practice
├── notebooks/         # Interactive Jupyter notebooks
└── code-samples/      # Standalone Python scripts
```

## 🎯 How to Use These Examples

### For Complete Beginners
1. Start with `notebooks/getting_started.ipynb` to set up your environment
2. Work through notebooks in order (numbered)
3. Run each cell and read the explanations carefully
4. Modify the code to see what happens!

### For Those with Some Experience
- Jump to notebooks that interest you
- Check specific code samples for reference
- Use datasets for your own experiments

## 📓 Jupyter Notebooks

Jupyter notebooks are interactive documents that combine code, visualizations, and explanations. They're perfect for learning!

### Getting Started
- **getting_started.ipynb**: Environment setup and Python basics
- Introduction to libraries (pandas, numpy, scikit-learn)
- Your first simple ML model with extensive comments

### Module-Specific Notebooks (Coming Soon)
As the course develops, we'll add notebooks for each module:
- **module-03-data-exploration.ipynb**: Loading and exploring data
- **module-04-data-preprocessing.ipynb**: Cleaning and preparing data
- **module-05-basic-models.ipynb**: Building your first ML models
- **module-06-explainability.ipynb**: Using SHAP and LIME for XAI
- And more!

## 💾 Datasets

Sample datasets are provided for practice. Each dataset includes:
- A README describing the data
- The data file(s) in CSV or other formats
- Information about the source and usage rights

### Available Datasets (Coming Soon)
- **iris-dataset/**: Classic flower classification
- **weather-prediction/**: Temperature forecasting example
- **medical-diagnosis-sample/**: Simplified medical data
- **crop-yield/**: Agricultural prediction dataset

**Note:** These are educational datasets. For real research, you'll use data from your field!

## 🐍 Code Samples

Standalone Python scripts demonstrating specific concepts:
- Data loading and basic operations
- Model training pipelines
- Evaluation and visualization
- XAI technique implementations

### How to Run Code Samples
```bash
# Navigate to the code-samples directory
cd examples/code-samples/

# Run a script
python script_name.py
```

## 🛠️ Setup Instructions

### 1. Install Python
Download Python 3.8+ from [python.org](https://www.python.org/downloads/)

### 2. Install Jupyter Notebook
```bash
pip install jupyter
```

Or use [Google Colab](https://colab.research.google.com/) - no installation needed!

### 3. Install Required Libraries
```bash
pip install pandas numpy scikit-learn matplotlib seaborn
```

For XAI examples:
```bash
pip install shap lime
```

### 4. Launch Jupyter Notebook
```bash
# Navigate to the examples/notebooks directory
cd examples/notebooks/

# Start Jupyter
jupyter notebook

# Your browser will open with the notebook interface
```

## 📚 Learning Path

Recommended order for working through examples:

1. **Start Here**: `getting_started.ipynb`
   - Set up your environment
   - Learn Python basics for ML
   - Run your first ML example

2. **Data Basics**: Explore datasets in the `datasets/` folder
   - Load different data formats
   - Understand data structure
   - Practice basic analysis

3. **Follow Modules**: Work through notebooks corresponding to course modules
   - Each notebook aligns with module content
   - Build practical skills as you learn concepts

4. **Experiment**: Modify examples and try your own ideas
   - Change parameters and see results
   - Apply techniques to your own data
   - Share your experiments in Discussions!

## 💡 Tips for Success

**Do:**
- ✅ Run every code cell yourself
- ✅ Read all comments carefully
- ✅ Modify code to see what happens
- ✅ Try with your own data when ready
- ✅ Ask questions if stuck

**Don't:**
- ❌ Just read without running code
- ❌ Copy-paste without understanding
- ❌ Skip the error messages (they teach you!)
- ❌ Rush through examples

## 🐛 Troubleshooting

### Problem: Jupyter won't start
**Solution:** Make sure it's installed: `pip install jupyter`

### Problem: Can't import libraries
**Solution:** Install missing libraries: `pip install library-name`

### Problem: Code produces an error
**Solution:** 
1. Read the error message carefully
2. Check if you ran all previous cells in order
3. Verify data files are in the right location
4. Ask in GitHub Discussions with the error message

### Problem: Using Google Colab
**Solution:** 
- Upload datasets to Colab
- Install libraries in the first cell: `!pip install library-name`
- All examples work in Colab!

## 🤝 Contributing Examples

Want to add your own examples? Great! Please:
1. Follow the coding style in existing examples
2. Include extensive comments explaining what the code does
3. Test your code thoroughly
4. Add a README if creating a new dataset
5. See [CONTRIBUTING.md](../CONTRIBUTING.md) for guidelines

## 📞 Need Help?

- **Code not working?** Check the Troubleshooting section above
- **Don't understand something?** Open a [Discussion](https://github.com/mahbubchula/XAI_TR/discussions)
- **Found a bug?** Open an [Issue](https://github.com/mahbubchula/XAI_TR/issues)

## 🔗 Additional Resources

- [Python for Beginners](https://www.python.org/about/gettingstarted/)
- [Jupyter Notebook Tutorial](https://jupyter.org/try)
- [Pandas Documentation](https://pandas.pydata.org/docs/)
- [Scikit-learn Tutorials](https://scikit-learn.org/stable/tutorial/index.html)

---

**Ready to start coding?** Open `notebooks/getting_started.ipynb` and begin your hands-on learning journey! 🚀
