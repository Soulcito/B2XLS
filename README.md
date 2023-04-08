# B2XLS

<h3 align="center">An easy way to export data to an excel file</h3>

<br />

<p align="center">
  <a href="https://opensource.org/licenses/MIT">
    <img src="https://img.shields.io/badge/License-MIT-blue.svg?style=flat-square" />
  </a>
  &nbsp;
</p>

<br />

## ⭐ Why B2XLS?

Most of the people who work in departments like accounting, operations, human resources, risk, finance, etc., use Excel in their daily work. In fact, many companies have software that delivers reporting and information to users, but they continue to validate said information in Excel, why? Because they have all the knowledge of the business and the software is made by developers where most He doesn't understand the business, but this is another topic.
B2XLS allows you to export data from different sources to an Excel spreadsheet, you concentrate the logic that you need to obtain from the databases in one place, which obviously allows you better maintenance when you need to change the logic and know where to have the data available for work them.

## ✨ Features

- Completely free and open-source
- Currently the connections are available for SQL Server, Oracle 18 or above, MySql 8
- All connections and script definitions in json files, very easy to understand.

<a target="_blank" href="https://github.com/Soulcito/B2XLS/discussions"><strong>Request Feature</strong></a>

## ✨ Prerequisites

Before beginning to work with B2XLS, you need to have instaled jave in your machine, probably you have installed.

- In the moment to build this tool, I have installed JDK 11.0.18 and JRE 1.8.
  [Installation Guide](https://docs.oracle.com/javase/10/install/toc.htm)
- [Download the tool, is a zip file.](https://github.com/Soulcito/B2XLS/tree/main/build)
- [Download the json files](https://github.com/Soulcito/B2XLS/tree/main/B2XLS)
- If you are a developer and you want to changue or view the source code, you need to work with [Talend Open Studio for Data Integration](https://www.talend.com/products/talend-open-studio/), and import the [LOCAL_PROJECT](https://github.com/Soulcito/B2XLS/tree/main/LOCAL_PROJECT). I use the 7.3 version.

## 🚀 Quick Start

- The json files must be into a C:/B2XLS folder

![b2xls folder](https://github.com/Soulcito/B2XLS/tree/main/img/b2xls_folder.png)

Don't worry about "output" and "log" folder, the tool will create it.

- The db.json file, is a referential file for what database you can use in the tool, here is important to know the "name" of each DB, an example:

![json file](https://github.com/Soulcito/B2XLS/tree/main/img/bd_json.png)

- The connection.json file is where you define all databases connection, an example:

![connection file](https://github.com/Soulcito/B2XLS/tree/main/img/connection_json.png)

- The query.json file is where you define all the scripts which will be executed in the databases. Here you can define the name of the excel file, in what sheet you want the data, an example:

![connection file](https://github.com/Soulcito/B2XLS/tree/main/img/query_json.png)
<br/><br/>
<b style=" color: red ">
Is important in this file fill the "fields" property, this data will be use in the header of the spreadsheet of each script
</b>
<br/><br/>
For example: You have the follow script

```sql
  select * from schema.table
```

OR

```sql
  select campo1, campo2, campo3 from schema.table
```

in the "fields" property you must to have

```json
  "fields": "campo1, campo2, campo3"
```

That is because in the open source version of TALEND, I don't have the obtain a dynamic schema for each script, so I solved this problem with the "fields" property.

## 🚨 Need help?

- [GitHub Discussions](https://github.com/Soulcito/B2XLS/discussions)
- [GitHub Issues](https://github.com/Soulcito/B2XLS/issues)
