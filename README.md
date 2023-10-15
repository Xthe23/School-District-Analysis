<h1>School District Analysis</h1>


<div class="center-div">
  <img src="https://github.com/Xthe23/pandas-challenge/blob/main/Images/education.png" alt="Education Image">
</div>


<p>
  This project provides an analysis of school district data, including student
  scores, budgets, and other relevant metrics.
</p>

Below is a snippet of the `PyCitySchools.ipynb` file used in this project. For the complete code, please [click here](https://github.com/Xthe23/pandas-challenge/blob/main/PyCitySchools/PyCitySchools.ipynb).

```python
per_school_summary = pd.DataFrame({
    "School Type": all_school_types,
    "Total Students": per_school_student_counts,
    "Total School Budget": per_school_budget,
    "Per Student Budget": per_school_student_capita,
    "Average Math Score": average_school_scores["math_score"],
    "Average Reading Score": average_school_scores["reading_score"],
    "% Passing Math": students_passing_math_percentage,
    "% Passing Reading": students_passing_reading_percentage,
    "% Overall Passing": students_passing_math_and_reading_percentage
})

# Display the DataFrame
per_school_summary
```
<h2>Dependencies and Setup</h2>
<p>To run the analysis, ensure you have the following dependencies:</p>
<pre><div class="bg-black rounded-md mb-4"><div class="flex items-center relative text-gray-200 bg-gray-800 gizmo:dark:bg-token-surface-primary px-4 py-2 text-xs font-sans justify-between rounded-t-md"><span>python</span><button class="flex ml-auto gizmo:ml-0 gap-2 items-center"><svg stroke="currentColor" fill="none" stroke-width="2" viewBox="0 0 24 24" stroke-linecap="round" stroke-linejoin="round" class="icon-sm" height="1em" width="1em" xmlns="http://www.w3.org/2000/svg"><path d="M16 4h2a2 2 0 0 1 2 2v14a2 2 0 0 1-2 2H6a2 2 0 0 1-2-2V6a2 2 0 0 1 2-2h2"></path><rect x="8" y="2" width="8" height="4" rx="1" ry="1"></rect></svg>Copy code</button></div><div class="p-4 overflow-y-auto"><code class="!whitespace-pre hljs language-python"><span class="hljs-keyword">import</span> pandas <span class="hljs-keyword">as</span> pd
<span class="hljs-keyword">from</span> pathlib <span class="hljs-keyword">import</span> Path
</code></div></div></pre>
<h2>Data Loading</h2>
<p>The data for this analysis comes from two CSV files:</p>
<ul>
  <li>
    <code>Resources/schools_complete.csv</code>: Contains data about each
    school, including its type, size, and budget.
  </li>
  <li>
    <code>Resources/students_complete.csv</code>: Contains data about each
    student, including their name, gender, grade, school, and scores in math and
    reading.
  </li>
</ul>
<h2>Data Processing</h2>
<p>
  The data from the two files is read into Pandas DataFrames and then merged on
  the <code>school_name</code> column to create a comprehensive dataset.
</p>
<h2>Key Metrics</h2>
<p>The analysis calculates several key metrics for the district:</p>
<ul>
  <li>Total number of schools</li>
  <li>Total number of students</li>
  <li>Total budget</li>
  <li>Average math and reading scores</li>
  <li>Percentage of students passing math, reading, and both subjects</li>
</ul>
<h2>School Summary</h2>
<p>For each school, the analysis calculates:</p>
<ul>
  <li>Type of school (District/Charter)</li>
  <li>Total number of students</li>
  <li>Total budget and budget per student</li>
  <li>Average math and reading scores</li>
  <li>Percentage of students passing math, reading, and both subjects</li>
</ul>
<h2>Top and Bottom Performing Schools</h2>
<p>
  Schools are ranked based on the percentage of students passing both subjects.
  The top 5 and bottom 5 schools are highlighted.
</p>
<h2>Scores by Grade</h2>
<p>
  Average math and reading scores are calculated for each grade level (9th to
  12th) at each school.
</p>
<h2>Scores by School Spending</h2>
<p>
  Schools are grouped into spending ranges based on their budget per student.
  For each spending range, the analysis calculates:
</p>
<ul>
  <li>Average math and reading scores</li>
  <li>Percentage of students passing math, reading, and both subjects</li>
</ul>
<h2>Scores by School Size</h2>
<p>
  Schools are grouped into size categories based on their total number of
  students. For each size category, the analysis calculates:
</p>
<ul>
  <li>Average math and reading scores</li>
  <li>Percentage of students passing math, reading, and both subjects</li>
</ul>
<hr />
