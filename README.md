# Automating_IDCard_Generation

## Overview  
This project automates the process of generating personalized ID cards using UiPath Studio. The workflow gathers data from an Excel sheet, processes images (e.g., employee photos), and generates ID cards with dynamic fields like name, designation, and ID number. The final ID cards are saved as image files and distributed via email.

## Features  
- **Excel Integration**: Reads input data (name, designation, image) from an Excel file.  
- **Image Processing**: Retrieves and processes employee photos for ID cards.  
- **Custom ID Card Template**: Generates ID cards with personalized details.  
- **Error Handling**: Includes Try-Catch blocks to handle missing images or invalid data.  
- **Output Distribution**: Sends generated ID cards via email using SMTP and stores them in designated directories.

## Prerequisites  
- UiPath Studio installed on your machine.  
- Access to an Excel file with the necessary user data (name, designation, photo, etc.).  
- Email configuration for SMTP (if email distribution is required).

## Workflow Description  
1. **Input Data Collection**: Data is collected from an Excel file using the Excel Application Scope and Read Range activities.  
2. **Image Processing**: Employee photos are read using the Read Image activity and processed for integration into the ID card template.  
3. **ID Card Design**: A custom ID card template is created with dynamic fields using Invoke Code or Invoke VBA to merge data and images.  
4. **Generate and Save ID Card**: The ID card is saved as an image file using the Save Image activity.  
5. **Output Distribution**: The ID card is emailed to the user or saved in a designated folder using the Send SMTP Mail Message and Copy File activities.  
6. **Error Handling**: Any exceptions during the process are handled using Try-Catch to ensure smooth execution.
