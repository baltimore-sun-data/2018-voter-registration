# Maryland voter registration analysis

By [Christine Zhang](mailto:czhang@baltsun.com)

The Baltimore Sun conducted an analysis of Maryland voter registration statistics from the state's Board of Elections.

The analysis provided information for the October 15, 2018 Baltimore Sun story titled ["Maryland nears record high voter registration — and independents make up the fastest-growing group"](http://www.baltimoresun.com/news/maryland/politics/bs-md-2018-voter-registration-20181011-story.html).

The Sun's findings and analysis are available in the "analysis" notebook in this repository, [`02_analysis.ipynb`]() (note: viewable on desktop).

https://twitter.com/baltsundata

## Data

The analysis uses information from the Maryland State Board of Elections [Monthly Voter Registration Activity Reports](https://elections.maryland.gov/voter_registration/stats.html). The state provides these reports as PDFs.

The cleaned CSV files are in the `output/` folder:
- `totals.csv`: total active registration, by county and party
- `changes.csv`: voter registration changes, by county and change type (address or name, or changes from* a particular party)
- `new.csv`: new registrations, by party and method of registration
- `removals.csv`: removals from the registered voter list, by party and reason for removal

\*The state does not track which party voters switched to.

Data was extracted from the January through September 2018 PDF reports (September 2018 was the most recent data available at the time of publication), and from the September 2014 and September 2016 reports (for a point-in-time comparison of 2018 with the most recent election years), using [Tabula](https://tabula.technology/), an open-source tool "for liberating data tables trapped inside PDF files."

The `01_processing.ipynb` notebook contains code that was used to process and combine the files for each month and year into cleaned data files for analysis.

Our story only uses the `totals.csv` file, but we have included the other files for completeness, so that others may conduct their own analyses.

The files in the `input/` folder correspond exactly to the columns in the PDF reports. The PDFs for each month and year are in the `pdf/` folder, for reference.

## Licensing

All code in this repository is available under the [MIT License](https://opensource.org/licenses/MIT). The data files are available under the [Creative Commons Attribution 4.0 International](https://creativecommons.org/licenses/by/4.0/) (CC BY 4.0) license.

![](page1.png)