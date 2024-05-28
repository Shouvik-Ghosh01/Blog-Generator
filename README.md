# Blog-Generator
Blog Generator

This code generates blog posts on a given topic using the LLaMA 2 large language model. Users can specify the topic, desired word count, and target audience (researchers, data scientists, or common people) to tailor the writing style.

Requirements

Streamlit library (https://docs.streamlit.io/)
langchain library (https://python.langchain.com/v0.1/docs/integrations/platforms/huggingface/)
langchain-community library (https://python.langchain.com/v0.1/docs/integrations/platforms/huggingface/)
Transformers library (likely installed with langchain-community)
Instructions

Install the required libraries:
Bash
pip install streamlit langchain langchain-community
Use code with caution.
content_copy
Save the code as blog_generator.py.
Run the script:
Bash
streamlit run blog_generator.py
Use code with caution.
content_copy
User Interface

The Streamlit app provides a user-friendly interface for generating blog posts:

Enter the Topic of the Blog: This text input field allows users to specify the topic of the blog post.
No of Words: This text input field lets users define the desired word count for the generated blog.
Writing the blog for: This dropdown menu offers three options: Researchers, Data Scientists, and Common People. Users can select the target audience to influence the writing style.
Generate: Clicking this button triggers the script to generate a blog post based on the provided inputs.
Output

If the user clicks "Generate," the app displays the generated blog post content below the button.

Code Breakdown

Imports: The code imports necessary libraries for Streamlit, Langchain, and the LLaMA 2 model.
getLLamaresponse function:
This function takes three arguments:
input_text: The topic of the blog post.
no_words: The desired word count.
blog_style: The target audience (researcher, data scientist, or common people).
It defines the LLaMA 2 model configuration and creates a prompt template incorporating the user-provided inputs.
The function calls the LLaMA 2 model with the formatted prompt and returns the generated response.
Streamlit App:
The app sets the page title, icon, layout, and initial sidebar state using st.set_page_config.
A header "Generate Blogs " is displayed using st.header.
Text input fields are created for capturing the blog topic and desired word count using st.text_input.
The app creates two columns to display the "No of Words" and "Writing the blog for" options using st.columns.
A dropdown menu is created using st.selectbox to allow users to choose the writing style.
A button "Generate" is created using st.button.
A conditional statement checks if the button is clicked (if submit). If yes, the getLLamaresponse function is called with the user inputs, and the generated response is displayed using st.write.
