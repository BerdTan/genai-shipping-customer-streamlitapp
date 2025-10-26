# 🚚 Smart Delivery Sentiment Dashboard

> **Unlock hidden insights in your delivery operations! Transform customer feedback into actionable business intelligence using Snowflake's AI-powered platform.**

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://genai-shipping-customer-app.streamlit.app/)

## 🎯 What This App Does

This intelligent dashboard analyzes **customer sentiment about delivery experiences** to help logistics and e-commerce teams optimize their operations. Built on Snowflake's modern data platform, it demonstrates how to rapidly prototype AI-driven business solutions.

### 📊 **Tab 1: Delivery Analytics Dashboard**
- **Sentiment vs Delivery Status** - Correlate customer satisfaction with delivery outcomes (In Transit, Processing, Delivered)
- **Product-Specific Analysis** - Identify which products have delivery-related satisfaction issues
- **Interactive Filtering** - Deep-dive into specific product categories or delivery statuses
- **Visual Insights** - Clear horizontal bar charts showing sentiment patterns

### 🔍 **Tab 2: Smart Query Engine (RAG)**
- **Natural Language Search** - Ask questions like "Any complaints about goggle deliveries?"
- **Contextual Results** - Get relevant customer review excerpts with source attribution
- **AI-Powered Insights** - Leverages Snowflake Cortex Search for intelligent document retrieval

---

## 🎓 Key Learning Takeaways

### **For Logistics & Operations Teams:**
- ✅ **Data-Driven Decisions** - Connect delivery performance directly to customer sentiment
- ✅ **Proactive Issue Detection** - Identify delivery problems before they escalate
- ✅ **Product-Specific Insights** - Understand which items need special handling

### **For Data Professionals:**
- ✅ **Rapid Prototyping** - From data to dashboard in minutes, not weeks
- ✅ **Modern RAG Implementation** - Build search capabilities without complex infrastructure
- ✅ **Snowflake Integration** - Leverage native AI services for enterprise-grade solutions

### **For Developers:**
- ✅ **Fast GenAI Development** - Prototype AI applications using modern tools
- ✅ **No Infrastructure Management** - Focus on business logic, not deployment complexity
- ✅ **Scalable Architecture** - Built on enterprise-ready data platform

### **For Business Leaders:**
- ✅ **Customer Experience Optimization** - Turn feedback into operational improvements
- ✅ **Cost-Effective Analytics** - Powerful insights without expensive custom development
- ✅ **Self-Service Intelligence** - Empower teams with interactive, AI-powered tools

---

## 🛠️ How to Set Up This App (for quick sense)

### **Prerequisites**
- Snowflake account with Streamlit and Cortex AI enabled
- Customer delivery dataset with sentiment scores
- Basic familiarity with Snowflake's interface

### **Quick Start (10 Minutes)**

#### **Step 1: Prepare Your Delivery Data**
```sql
-- Create your workspace
CREATE DATABASE AVALANCHE_DB;
CREATE SCHEMA AVALANCHE_DB.AVALANCHE_SCHEMA;

-- Your table should include columns like:
-- PRODUCT, SENTIMENT_SCORE, STATUS (On Time/Late/Damaged), REVIEW_TEXT
CREATE TABLE REVIEWS_WITH_SENTIMENT (
    PRODUCT VARCHAR(100),
    SENTIMENT_SCORE FLOAT,
    STATUS VARCHAR(50),
    REVIEW_TEXT TEXT,
    -- Add other relevant columns
);
```

#### **Step 2: Set Up AI Search Capabilities**
```sql
-- Create chunks table for RAG functionality
CREATE TABLE customer_review_chunks (
    CHUNK TEXT,
    file_name VARCHAR(255)
);

-- Create Cortex Search Service
CREATE CORTEX SEARCH SERVICE AVALANCHE_SEARCH_SERVICE
ON customer_review_chunks
WAREHOUSE = YOUR_WAREHOUSE;
```

#### **Step 3: Deploy the App**
1. **Upload Code**: Copy [`appsnowsen.py`](appsnowsen.py) to Snowflake Streamlit
2. **Configure Database**: Update database/schema names if different
3. **Test Connection**: Ensure data loads properly
4. **Launch**: Deploy as Streamlit in Snowflake application
5. **Explore**: Try the live demo at [https://genai-shipping-customer-app.streamlit.app/](https://genai-shipping-customer-app.streamlit.app/)

### **Customization for Your Data**
- **Delivery Statuses**: Modify to match your logistics categories (Delivered, Delayed, Lost, etc.)
- **Sentiment Scale**: Adjust for your sentiment analysis range
- **Product Categories**: Customize filtering for your product catalog
- **Visual Themes**: Apply your company branding

---

## 📚 Resources & Learning Path

### **🎓 Learn the Fundamentals**
- **Deep Learning AI Course**: [Fast Prototyping of GenAI Apps with Streamlit](https://learn.deeplearning.ai/courses/fast-prototyping-of-genai-apps-with-streamlit/lesson/jclt75/conversation-between-chanin-nantasenamat-and-andrew-ng)
  - *Perfect starting point for understanding rapid GenAI development like this one*
  - *there are sample data for trying out this apps*

### **🛠️ Technical Documentation**
- **Snowflake Streamlit**: [Official Deployment Guide](https://docs.snowflake.com/en/developer-guide/streamlit/about-streamlit)
- **Cortex AI Services**: [Snowflake AI Documentation](https://docs.snowflake.com/en/user-guide/snowflake-cortex/overview)
- **Streamlit Cloud**: [Community Deployment Guide](https://docs.streamlit.io/streamlit-community-cloud)

### **🚀 Deployment Options**
- **Streamlit Community Cloud**: [Free deployment platform](https://share.streamlit.io/)
- **Snowflake Native**: [Deploy within your data warehouse](https://docs.snowflake.com/en/developer-guide/streamlit/create-streamlit-app)
- **Self-Hosted**: [Custom deployment solutions](https://docs.streamlit.io/knowledge-base/deploy)

### **💡 Advanced Learning**
- **RAG Architecture**: Understanding Retrieval-Augmented Generation patterns
- **Data Visualization**: Advanced Streamlit charting techniques
- **AI Integration**: Connecting business processes with GenAI capabilities

---

## 💡 Pro Tips for Delivery Analytics

### **📊 Data Quality Matters**
- **Consistent Categorization**: Standardize delivery status labels
- **Sentiment Calibration**: Ensure sentiment scores align with business understanding
- **Regular Updates**: Keep data fresh for accurate trend analysis

### **🔍 Smart Querying**
- **Specific Questions**: Try "Which products have the most delivery complaints?"
- **Trend Analysis**: Ask about seasonal delivery performance patterns
- **Root Cause**: Query for specific delivery failure reasons

### **🚀 Scaling Your Implementation**
- **Start with Key Products**: Focus on high-volume or high-value items first
- **Monitor Performance**: Track Snowflake credits during development
- **User Training**: Provide guidance on effective query formulation

---

## 🌟 Next Steps

1. **🎮 Try the Demo**: [Explore the live application](https://genai-shipping-customer-app.streamlit.app/)
2. **📚 Explore the Course**: [Learn GenAI prototyping fundamentals](https://learn.deeplearning.ai/courses/fast-prototyping-of-genai-apps-with-streamlit/)
3. **🔧 Clone & Customize**: Adapt this solution for your specific delivery data
4. **🚀 Deploy & Scale**: Roll out to your team and gather feedback

---

**Transform your delivery data into competitive advantage with AI :)** 
[🚀 Start exploring now](https://genai-shipping-customer-app.streamlit.app/)

---
