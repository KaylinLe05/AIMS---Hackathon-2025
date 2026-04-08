# AIMS Hackathon - Light Carriers
This repository contains research and development by Gongpals Team under the project named Light Carriers, which provides data-driven solutions addressing modern slavery detection, analysis, and prevention. Our project aims to leverage data analytics and visualization to combat one of the world's most pressing human rights challenges.
Mission
Developing a comprehensive analytics platform to increase awareness, improve detection capabilities, and support evidence-based policy making, NGOs, stakeholders in the fight against modern slavery.

# 1. Problem Statement

**The Problem**

Thousands of companies publish Modern Slavery Statements annually—comprehensive reports spanning hundreds of pages. Yet despite this massive volume of documentation, these reports consistently fail to deliver actionable transparency. The core issue isn't quantity; it's quality. Reports are plagued by ambiguous language, inconsistent frameworks, and incomplete disclosures that obscure rather than illuminate corporate practices.

**The Impact**

This transparency deficit creates a multi-stakeholder crisis:
- Policy makers struggle to identify patterns across an ocean of unstructured text.
- NGOs cannot extract concrete evidence from vague corporate communications.
- Businesses operate without clear benchmarks or visibility into industry best practices.
- Researchers face barriers to meaningful trend analysis and evidence-based recommendations.

**The Opportunity**

With tens of thousands of reports already published, we have a massive repository of trapped intelligence. The time is ripe for a transformative solution that converts regulatory compliance into meaningful, actionable transparency.


# 2. Objective
Objective of the solutions (the challenge, problem or need that it contributes to solve).
Primary Challenge/Problem Statement

Core issue: Modern slavery statements create information overload without actionable insights

## **Specific solution address**

Data Extraction: Converting unstructured text into structured, analyzable data
Standardization: Creating consistent metrics across different reporting frameworks
Accessibility: Making complex information digestible for various stakeholder groups
Comparative Analysis: Enabling benchmarking and trend identification across companies/sectors

## **Target User Problems**

Policy makers: Need to identify patterns and evaluate regulatory effectiveness
NGOs: Require concrete evidence for advocacy and oversight
Businesses: Want to benchmark against peers and identify best practices
Researchers: Need data for trend analysis and evidence-based recommendations

## **Solution Contribution Goals**

Transform regulatory compliance documents into actionable intelligence
Enable real-time monitoring and assessment of corporate commitments
Facilitate evidence-based decision making across stakeholder groups
Bridge the gap between legal compliance and meaningful transparency

## **Expected Outcomes**
Improved stakeholder access to meaningful modern slavery risk information
Enhanced corporate accountability through transparent performance comparison
More effective policy development based on data-driven insights
Strengthened advocacy efforts through accessible evidence base


# 3. Solution/Data use case description
A comprehensive description of the data-based solution or/and data use case.

### **Solution Overview**

There are 3 available data-based solutions: 

- **Comprehensive industrial data analytics and index dashboard** that transforms raw modern slavery compliance data into actionable insights for businesses, regulators, and stakeholders. The solution consists of two interconnected dashboards that provide different perspectives on modern slavery reporting and compliance. 
- **Individual document intelligence** This AI-powered solution utilizes advanced large language models (LLMs) and proprietary data analytics to transform companies' modern slavery statements into quantified compliance scores, standardized metrics, comprehensive visualizations, and targeted recommendations for improvement.
- **AI chatbot**: This intelligent conversational platform transforms traditional passive information consumption into dynamic, interactive learning experiences. The AI chatbot leverages comprehensive compliance datasets to help users transition from passive scrolling to active engagement with modern slavery compliance resources and requirements.

---

## **1. Data Architecture & Sources**

### **Primary Data Sources:**
- **AIMS-derived CSV files** - Core compliance data from the Australian Modern Slavery Index
- **Criteria-specific summaries** - 7 CSV files (criteria1-7_final_summary.csv) containing detailed performance metrics
- **Sector analysis data** - `au_uk_unified_sectors_merged.csv` with sector-specific compliance data
- **Derived analytics** - Processed datasets including `policy_vs_action_by_sector.csv`, `disclosure_by_sector.csv`

### **Data Structure:**
- **Company-level data** - Individual company compliance scores and metrics
- **Sector-level aggregation** - Industry-specific performance analysis
- **Criteria-based breakdown** - 7 international reporting criteria with detailed metrics
- **Temporal analysis** - Multi-year compliance trends and patterns

---

## **2. Solution**

### **Dashboard 1: Modern Slavery Index (index.py)**
**Purpose:** Global perspective and interactive exploration

**Key Features:**
- **Interactive World Map** - Visual representation of modern slavery prevalence globally
- **Country/State Analysis** - Detailed breakdown by geographical regions
- **Multi-metric Visualization** - Modern Slavery Index, Rate per 1000, and Case counts
- **Advanced Filtering** - By slavery types, thresholds, and specific metrics
- **Real-time Hover Data** - Comprehensive metrics on country selection

**Data Use Cases:**
- **Policy Makers** - Understanding global modern slavery patterns
- **Researchers** - Analyzing regional variations and trends
- **NGOs** - Identifying high-risk areas for intervention
- **Media** - Creating compelling visualizations for public awareness

**How Data is Used:**
- **Sample Data Generation** - Creates synthetic modern slavery data for 20 countries with realistic metrics
- **Geographic Mapping** - Uses country names and coordinates to create choropleth world maps
- **Multi-metric Display** - Combines Modern Slavery Index, Rate per 1000, and Case counts in hover tooltips
- **Dynamic Filtering** - Applies user-selected filters to subset and visualize data
- **State/Regional Analysis** - Uses predefined coordinates for Australian states, US states, and UK cities

### **Dashboard 2: Business Compliance Analytics (modern_slavery_dashboard.py)**
**Purpose:** Corporate compliance analysis across business sectors

**Key Features:**
- **7-Criteria Analysis** - Detailed breakdown of international reporting standards
- **Policy vs Action Gap Analysis** - Identifying implementation challenges
- **Sector Benchmarking** - Industry-specific performance comparisons
- **Boilerplate Content Detection** - Quality assessment of compliance disclosures
- **Export & Reporting** - Downloadable data and reports

**Data Use Cases:**
- **Corporate Compliance Teams** - Benchmarking against industry standards
- **Regulators** - Monitoring compliance across sectors
- **Investors** - ESG risk assessment and due diligence
- **Consultants** - Providing compliance advisory services

**How Data is Used:**
- **CSV Data Integration** - Loads `criteria1-7_final_summary.csv` files for detailed performance metrics
- **Sector Analysis** - Uses `au_uk_unified_sectors_merged.csv` for industry-specific breakdowns
- **Policy vs Action Analysis** - Processes `c4_ms_remediation__bool` and `c4_risk_mitigation__bool` columns to identify implementation gaps
- **Derived Metrics** - Generates `policy_vs_action_by_sector.csv` and `disclosure_by_sector.csv` for advanced analytics
- **Compliance Scoring** - Calculates achievement percentages and weighted compliance scores by sector
- **Boilerplate Detection** - Analyzes text content to identify generic vs substantive policy language

### **Individual Document Intelligence**
**Purpose:** AI-powered analysis of individual company modern slavery statements and compliance documents

**Key Features:**
- **Document Processing** - Automated extraction and analysis of company statements
- **Content Analysis** - AI-powered assessment of policy substance vs boilerplate content
- **Compliance Scoring** - Individual document scoring against 7 international criteria
- **Gap Identification** - Automated detection of missing or weak compliance elements
- **Trend Analysis** - Historical analysis of company statement improvements over time

**Data Use Cases:**
- **Compliance Officers** - Automated review of company statements for completeness
- **Regulators** - Efficient screening of compliance documents for quality and substance
- **Investors** - Due diligence analysis of company modern slavery commitments
- **Consultants** - Rapid assessment of client compliance documentation quality
- **Researchers** - Large-scale analysis of corporate modern slavery reporting patterns

**How Data is Used:**
- **Document Parsing** - Processes PDF and text files to extract structured compliance information
- **Text Mining** - Uses NLP techniques to identify key compliance elements and policy components
- **Criteria Mapping** - Maps document content to the 7 international reporting criteria
- **Content Classification** - Categorizes text as substantive policy vs boilerplate content
- **Scoring Algorithm** - Generates quantitative scores based on presence and quality of compliance elements
- **Comparative Analysis** - Benchmarks individual documents against industry standards and best practices

### **AI Chatbot**
**Purpose:** Intelligent conversational interface for modern slavery compliance guidance and data exploration

**Key Features:**
- **Natural Language Queries** - Users can ask questions in plain English about compliance data
- **Contextual Responses** - Provides relevant insights based on user's specific sector, company size, or compliance level
- **Interactive Data Exploration** - Guides users through complex datasets with conversational interface
- **Compliance Guidance** - Offers specific recommendations based on current performance metrics
- **Real-time Analysis** - Processes user queries against live dashboard data

**Data Use Cases:**
- **Business Users** - Quick answers to compliance questions without technical expertise
- **Compliance Teams** - Interactive guidance on improving specific criteria performance
- **Researchers** - Natural language exploration of complex compliance datasets
- **Regulators** - Efficient querying of compliance data for enforcement decisions
- **Students/Educators** - Learning tool for understanding modern slavery compliance

**How Data is Used:**
- **Query Processing** - Converts natural language questions into SQL queries against dashboard databases
- **Data Integration** - Combines information from multiple CSV files and derived datasets
- **Context Awareness** - Uses user's sector, company, or criteria focus to filter and prioritize responses
- **Real-time Analytics** - Processes live data from `criteria2_final_summary.csv` and sector performance files
- **Pattern Recognition** - Identifies common questions and provides proactive insights based on data trends
- **Response Generation** - Synthesizes data from multiple sources to provide comprehensive, contextual answers
- **Learning Adaptation** - Tracks user interactions to improve response relevance and accuracy over time

---

## **3. Core Data Analytics Capabilities**

### **Compliance Scoring System:**
- **Quantitative Metrics** - Achievement percentages across 7 criteria
- **Qualitative Analysis** - Policy substance vs boilerplate content detection
- **Sector Normalization** - Weighted compliance scores by industry
- **Trend Analysis** - Multi-year performance tracking

### **Advanced Analytics Features:**
- **Policy-Action Gap Analysis** - Identifying companies with policies but no implementation
- **Boilerplate Detection** - Flagging generic, non-specific compliance language
- **Sector Performance Benchmarking** - Industry-specific compliance comparisons
- **Risk Assessment** - Identifying high-risk companies and sectors

### **Data Quality Management:**
- **Automated Data Validation** - Ensuring data integrity and consistency
- **Missing Data Handling** - Graceful degradation for incomplete datasets
- **Data Source Attribution** - Clear tracking of data origins and reliability
- **Quality Warnings** - User alerts for data limitations

---

## **4.Benchmarking Features**

### **Key Performance Indicators (KPIs):**
- **Overall Compliance Rate** - Aggregate performance across all criteria
- **Sector Performance Rankings** - Industry-specific compliance scores
- **Policy Implementation Rate** - Percentage of companies with actionable policies
- **Gap Analysis Metrics** - Policy vs action implementation rates

### **Predictive Analytics:**
- **Compliance Trend Forecasting** - Predicting future performance based on historical data
- **Risk Scoring** - Identifying companies at risk of non-compliance
- **Sector Impact Analysis** - Understanding how sector changes affect compliance

### **Benchmarking Capabilities:**
- **Peer Comparison** - Company vs industry performance
- **Best Practice Identification** - Learning from top performers
- **Gap Analysis** - Identifying specific improvement areas
- **Progress Tracking** - Monitoring compliance improvements over time

---

## **5. Technical Implementation**

### **Data Processing Pipeline:**
- **ETL Processes** - Automated data extraction, transformation, and loading
- **Data Validation** - Quality checks and error handling
- **Aggregation Logic** - Sector and criteria-based data summarization
- **Real-time Updates** - Dynamic data refresh and visualization updates

### **Visualization Engine:**
- **Interactive Charts** - Plotly-based dynamic visualizations
- **Geographic Mapping** - Choropleth maps for global data representation
- **Custom Styling** - Professional, branded dashboard appearance
- **Responsive Design** - Multi-device compatibility

### **Export & Reporting:**
- **Data Export** - CSV downloads for further analysis
- **Report Generation** - Automated compliance reports
- **Custom Filtering** - User-specific data extraction
- **API Integration** - Potential for third-party system integration

---

## **6. Impact & Value Proposition**

### **For Businesses:**
- **Compliance Optimization** - Streamlined compliance monitoring and reporting
- **Risk Mitigation** - Proactive identification and management of modern slavery risks
- **Competitive Advantage** - Benchmarking against industry peers
- **Stakeholder Confidence** - Transparent, data-driven compliance reporting

### **For Regulators:**
- **Efficient Monitoring** - Automated compliance tracking across sectors
- **Data-Driven Enforcement** - Evidence-based regulatory actions
- **Policy Effectiveness** - Measuring impact of regulatory interventions
- **Resource Optimization** - Targeted compliance efforts where most needed

### **For Society:**
- **Transparency** - Public access to compliance information
- **Accountability** - Holding companies accountable for their actions
- **Progress Tracking** - Measuring collective progress against modern slavery
- **Awareness** - Raising public awareness through data visualization

This comprehensive data-based solution transforms complex modern slavery compliance data into actionable insights, enabling evidence-based decision-making across multiple stakeholders and use cases.

# 4. Pitch
Location: [link to video](https://www.youtube.com/watch?v=yjOPOFmy9q8)

# 5. Datasets
Location: [/datasets](https://github.com/KaylinLe05/AIMS---Hackathon-2025/tree/main/dataset-main)

# 6. Project Code
Location: [/project](https://github.com/KaylinLe05/AIMS---Hackathon-2025/tree/main/AIMS-hackathon-main)

# 7. Additional docs 
Location: [/docs](https://docs.google.com/document/d/1J4SoxbSQwzZsAuCLYhQRMdBqm_6Oyq9A6mO6pdSrsMY/edit?usp=sharing)

# 8. Declaration of Intellectual Property
Many thanks to the organizations and people who compiled resources that we refer to in our project, including:

-Beyond Compliance_ Walk Free  
-Wikirate -AIMS.au
-Fair Work Ombudsman
-United Nation
-Australian Government
-Research and Documents from Universities around the World about Modern Slavery

# This project builds on the open research of Project AIMS (AI against Modern Slavery) by Mila and QUT.  
GitHub repository: [ai4h_aims-au](https://github.com/mila-ai4h/ai4h_aims-au).
# Disclaimers  
### Computational Resources & Comparative Results  
- Describe here the resources used in developing your solution (e.g. GPUs, etc).  

### No Claims About Companies  
This repository and its accompanying models, datasets, metrics, dashboards, and comparative analyses are provided strictly for research and demonstration purposes.  

Any comparisons, rankings, or assessments of companies or organizations are exploratory in nature. They may be affected by incomplete data, modeling limitations, or methodological choices. These results must not be used to make factual, legal, or reputational claims about any entity without independent expert review and validation.  

Do not use this repository’s contents to make public statements or claims about specific companies, organizations, or individuals.  


# Terms and Conditions
By submitting this solution to the AIMS Hackathon, our team acknowledges and agrees to abide by the Event’s [Terms and Conditions](https://fundacionpasoslibres.org/wp-content/uploads/AIMS-Hackathon-Terms-and-Conditions-2025-1.pdf).


