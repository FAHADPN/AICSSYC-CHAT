# Inquiry Bot Documentation

## Table of Contents

1. **Introduction**
   - 1.1. Overview
   - 1.2. Purpose
   - 1.3. Scope

2. **Bot Architecture**
   - 2.1. Botpress Workflow
   - 2.2. StackAI Integration

3. **Data Sources**
   - 3.1. AICSSYC '23 Website
   - 3.2. Previous AICSSYC Data
   - 3.3. Data Scraping with Apify

4. **Integration**
   - 4.1. Website Integration
   - 4.2. User Interaction Flow

5. **Technical Details**
   - 5.1. Botpress Configuration
   - 5.2. StackAI Configuration
   - 5.3. GPT-3.5-turbo Model
   - 5.4. Vector Database

6. **Usage Instructions**
   - 6.1. Starting the Chatbot
   - 6.2. User Interactions
   - 6.3. Stopping the Chatbot

7. **Maintenance and Troubleshooting**
   - 7.1. Data Updates
   - 7.2. Handling Errors

8. **Conclusion**
   - 8.1. Future Enhancements

## 1. Introduction

### 1.1. Overview

This documentation provides a detailed insight into the Inquiry Bot developed for AICSSYC '23. The bot is created using OpenAI GPT-3.5-turbo and integrated into Botpress, a conversational AI software. It serves as a powerful tool for answering queries related to AICSSYC '23 and previous editions.

### 1.2. Purpose

The primary purpose of this bot is to provide accurate and timely information to users about AICSSYC '23 and past editions. It leverages AI and web scraping technologies to gather data and generate responses.

### 1.3. Scope

This documentation covers the bot's architecture, data sources, integration with the AICSSYC '23 website, technical details, usage instructions, and maintenance procedures.

## 2. Bot Architecture

### 2.1. Botpress Workflow

The bot's interaction with users follows this workflow:


User Message &rarr; Greets user and Asks user to prompt &rarr; User prompts &rarr; User prompt is sent to StackAI &rarr; StackAI **response** is displayed to the user &rarr; Repeat until user types stop or exit


### 2.2. StackAI Integration

StackAI acts as an intermediary between Botpress and GPT-3.5-turbo:


Input prompt sent by Botpress &rarr; Document (Previous AICSSYC's) & AICSSYC '23 website data &rarr; Converted to Vector DB &rarr; Vector DB sent to GPT-3.5-turbo along with the user prompt &rarr; Response received and sent to Botpress


## 3. Data Sources

### 3.1. AICSSYC '23 Website

Data for AICSSYC '23 is sourced directly from the official website.

### 3.2. Previous AICSSYC Data

Data from previous AICSSYC editions is scraped from Facebook using the Facebook posts scraper in Apify.

### 3.3. Data Scraping with Apify

Apify is utilized for web scraping and automation. It extracts data from websites and automates tasks, making it a valuable tool for gathering historical data.

## 4. Integration

### 4.1. Website Integration

The chatbot is integrated into a clone of the current AICSSYC '23 website. This integration allows users to interact with the bot seamlessly while browsing the event's web pages.

### 4.2. User Interaction Flow

Users start a conversation with the bot through the website, and their prompts are processed by Botpress. StackAI handles the data retrieval and interaction with the GPT-3.5-turbo model, providing users with responses.

## 5. Technical Details

### 5.1. Botpress Configuration

Botpress is configured to handle user prompts, greetings, and exiting commands. It acts as the user interface for the bot.

### 5.2. StackAI Configuration

StackAI is set up to preprocess data from different sources, create a Vector Database, and communicate with the GPT-3.5-turbo model.

### 5.3. GPT-3.5-turbo Model

OpenAI's GPT-3.5-turbo model is employed to generate responses to user queries. It is a powerful language model capable of understanding and generating human-like text.

### 5.4. Vector Database

The Vector Database contains preprocessed data from AICSSYC '23 and previous editions, allowing for efficient querying by the bot.

## 6. Usage Instructions

### 6.1. Starting the Chatbot

Users can initiate a conversation with the bot by visiting the AICSSYC '23 website and clicking on the chat icon. The bot will greet the user and ask for a prompt.

### 6.2. User Interactions

Users can interact with the bot by typing prompts or questions related to AICSSYC '23 or previous editions. The bot will provide responses based on the input.

### 6.3. Stopping the Chatbot

Users can stop the conversation at any time by typing "stop" or "exit." The bot will acknowledge and end the session.

## 7. Maintenance and Troubleshooting

### 7.1. Data Updates

To keep the bot's knowledge up-to-date, regular updates from the AICSSYC '23 website and Facebook scraping for previous editions may be necessary.

### 7.2. Handling Errors

Proper error handling mechanisms should be in place to address any issues that may arise during bot interactions. Logs and alerts can help in monitoring and troubleshooting.

## 8. Conclusion

### 8.1. Future Enhancements

The Inquiry Bot for AICSSYC '23 provides a valuable resource for users seeking information about the event. Future enhancements may include natural language understanding improvements, support for more data sources, and enhanced error handling for an even better user experience.