# 🎨 MoMA Art Analytics Dashboard (Power BI)
# 📌 1. Project Overview

This project presents an interactive Power BI dashboard built using the Museum of Modern Art (MoMA) dataset from Maven Analytics.

The dashboard analyzes:

Artist demographics

Artwork classifications

Acquisition trends

Department distribution

Gender representation

Nationality insights

The objective is to transform raw art collection data into meaningful visual insights using Power BI and DAX.

# 📊 2. Dataset Description

The project uses two cleaned datasets:

🔹 Artists Table

DisplayName

Gender

Nationality

BeginDate

EndDate

ConstituentID

ArtistBio

🔹 Artworks Table

Title

Artist

Classification

Department

DateAcquired

Medium

Height (cm)

Width (cm)

ImageURL

ObjectID

ConstituentID

🔗 Data Model Relationship
Artists[ConstituentID] 1  →  ∞ Artworks[ConstituentID]

This relationship allows artist attributes (Gender, Nationality, etc.) to filter artwork data dynamically.

# 📈 3. Dashboard Features
🔹 Key Performance Indicators (KPIs)

Total Artworks

Total Artists

Total Departments

Total Classifications

Most Featured Artist

Male Artist Count

Female Artist Count

Total Mediums

🔹 Visualizations Included
📅 Trend Analysis

Total Artworks by Year

Total Artworks by Month

Acquisition Period Analysis

🎨 Classification Analysis

Artworks by Classification (Treemap / Bar Chart)

Artworks by Department

👩‍🎨 Artist Analysis

Total Artists by Nationality

Total Artists by Age Group

Most Featured Artists

⚖ Gender Analysis

Male vs Female Distribution

Gender-based filtering using slicers

🖼 Image Integration

Artwork Image display using ImageURL field

# 🧮 4. DAX Measures Used
Total Artworks = COUNTROWS(Artworks)

Total Artists = COUNTROWS(Artists)

Artwork Count = COUNT(Artworks[ObjectID])

Female Artist % =
DIVIDE(
    CALCULATE(COUNTROWS(Artists), Artists[Gender] = "Female"),
    COUNTROWS(Artists)
)

Avg Artwork Year = AVERAGE(Artworks[BeginDate])

Additional measures were created for:

Age group calculation

Acquisition period grouping

Most featured artist calculation

# 🎨 5. Dashboard Design & Theme
🎨 Color Palette

Navy — #14213D

Gold — #FCA311

Off-white — #E5E5E5

Gray — #3D3D3D

🖌 Design Approach

Dark museum-style background

Highlighted KPI cards

Clean typography

Interactive slicers for dynamic filtering

Balanced layout for professional presentation

# 🎯 6. Key Insights

American artists dominate the collection.

Prints and Photography are among the most common classifications.

Acquisition trends vary significantly across historical periods.

Male artists outnumber female artists, but female representation is visible.

Certain artists contribute disproportionately to total artworks.

# 🛠 7. Tools & Technologies Used

Power BI Desktop

DAX (Data Analysis Expressions)

Power Query (Data Cleaning)

Maven Analytics MoMA Dataset

# 📷 8. Dashboard Preview

(Add dashboard screenshots here)

# 🚀 9. How to Use

Download or clone this repository.

Open the .pbix file in Power BI Desktop.

Refresh the dataset if required.

Use slicers and filters to explore insights interactively.
