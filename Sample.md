# Text

It's very easy to make some words **bold** and other words *italic* with Markdown. You can even [link to Google!](http://google.com)

# Headers

# This is an \<h1> tag
## This is an \<h2> tag
#### This is an \<h4> tag

*This text will be italic*<br/>
_This will also be italic_<br/>

**This text will be bold**<br/>
__This will also be bold__<br/>

_You **can** combine them_<br/>

# Lists

## Unordered

* Item 1
* Item 2
  * Item 2a
  * Item 2b

## Ordered

1. Item 1
1. Item 2
1. Item 3
   1. Item 3a
   1. Item 3b

# Images

![GitHub Logo](/images/logo.png)
![Image of Yaktocat](/images/yaktocat.png)

# Links

http://github.com - automatic!
[GitHub](http://github.com)

# Blockquotes

> "My mama always said life was like a box of chocolates. You never know what  you're gonna get."<br/>Forrest Gump, 1994

# Inline Code
```javascript
if (isAwesome){
  return true
}
```
```xml
<?xml version="1.0" encoding="utf-16" ?>
<BatchDataSyncConfig name="SALESFORCE_PEOPLE_TARGET" version="1.0.0" 
	xmlns="http://www.cinchy.co">
	   <Parameters>
        <Parameter name="authUrl" />
        </Parameters>
	<CinchyQueryDataSource domain="Sandbox" name="Get_People">
		<Schema>
			<!-- <Column name="Salesforce Id" dataType="Text" /> -->
			<Column name="FirstName" dataType="Text"/>
			<Column name="LastName" dataType="Text"/>
			<Column name="Company" dataType="Text" />
			<Column name="Title" dataType="Text" />
		</Schema>
	</CinchyQueryDataSource>
	<SalesforceTarget object="Contact" authUrl="@authUrl" clientId="RCgdSrllHcsn40rynBWDDDAP1StSBYKLiASUv+HwUk4mgIh2CuUzb1qff+hBVjLU0yt79r9Dz+ZKuBebmv4yeP7GbIssHP2AVcMj3NBKj4JxPhM20JdviyrN1GtwZMynYKRRnP6nk/+hKQxVOH7+Zg==" clientSecret="F57hfsH0fzYQZuyOuWu5wVA6U6dGIMuBicrwwdBVU77XcqKLTJtnz9OFuMq1TSTVFiQGxUMw9ht3KvCrmMUTHIP3cnzOpIhcMeMWHbZtEjthQXCAjxO7bbG3JPfzqEy8" username="p+oJ16uYGorl5vtTkz6wKXL8YLyooIFRGvT58kKVZ9gjGKgLbTozgV/v6i7LO9Fl" password="ErEyavgJxgNUHk1VtcJr1iS5JPnxoQJWncx4Dj+AMoM="  suppressDuplicateErrors="true">
		<ColumnMappings>
			<!-- <ColumnMapping sourceColumn="Salesforce Id" targetColumn="Id" /> does not work-->
			<ColumnMapping sourceColumn="FirstName" targetColumn="FirstName" />
			<ColumnMapping sourceColumn="LastName" targetColumn="LastName" />
			<ColumnMapping sourceColumn="Company" targetColumn="AccountId" />
			<ColumnMapping sourceColumn="Title" targetColumn="Title" />
		</ColumnMappings>
		<SyncKey>
			<SyncKeyColumnReference name="FirstName" />
			<SyncKeyColumnReference name="LastName" />
		</SyncKey>

		<NewRecordBehaviour type="INSERT" />
		<ChangedRecordBehaviour type="UPDATE" />
		<DroppedRecordBehaviour type="IGNORE" />
	</SalesforceTarget>
</BatchDataSyncConfig>
```

# Task Lists

- [x] This is a complete item
- [ ] This is an incomplete item

# Tables
  
First Header | Second Header
------------ | -------------
Content from cell 1 | Content from cell 2
Content in the first column | Content in the second column