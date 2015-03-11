vazco:universe-autoform-select
=========================

An add-on Meteor package for [aldeed:autoform](https://github.com/aldeed/meteor-autoform). Provides a single custom input type, "universe-select".

## Prerequisites

The plugin library must be installed separately.

In a Meteor app directory, enter:

```bash
$ meteor add aldeed:autoform
```

## Installation

In a Meteor app directory, enter:

```bash
$ meteor add vazco:universe-autoform-select
```

## Usage

Specify "universe-select" for the `type` attribute of any input. This can be done in a number of ways:

In the schema, which will then work with a `quickForm` or `afQuickFields`:

```js
{
  tags: {
    type: [String],
    autoform: {
      type: "universe-select",
      afFieldInput: {
        multiple: true
      }
    }
  }
}
```

Or on the `afFieldInput` component or any component that passes along attributes to `afFieldInput`:

```js
{{> afQuickField name="tags" type="universe-select" multiple=true}}

{{> afFormGroup name="tags" type="universe-select" multiple=true}}

{{> afFieldInput name="tags" type="universe-select" multiple=true}}
```

## Options



<table width="100%">
	<tr>
		<th valign="top" colspan="4" align="left"><a href="#general" name="general">universe-select options</a></th>
	</tr>
	<tr>
		<th valign="top" width="120px" align="left">Option</th>
		<th valign="top" align="left">Description</th>
		<th valign="top" width="60px" align="left">Type</th>
		<th valign="top" width="60px" align="left">Default</th>
	</tr>
	<tr>
		<td valign="top"><code>options</code></td>
		<td valign="top"><i>Required.</i> A function returning either an array of options, or a <code>Mongo.Cursor</code>. The function is re-evaluated automatically using <code>Tracker</code> when its reactive data sources change.</td>
		<td valign="top"><code>function</code></td>
		<td valign="top"><code>undefined</code></td>
	</tr>
	<tr>
		<td valign="top"><code>placeholder</code></td>
		<td valign="top"><i>Optional.</i> A placeholder option with empty value will be added as first element of the options collection. It can be used with selectize.js's <code>allowEmptyOption</code> setting.</td>
		<td valign="top"><code>object</code></td>
		<td valign="top"><code>undefined</code></td>
	</tr>
	<tr>
		<td valign="top"><code>multiple</code></td>
		<td valign="top"><i>Optional.</i> </td>
		<td valign="top"><code>Boolean</code></td>
		<td valign="top"><code>undefined</code></td>
	</tr>
	<tr>
        <td valign="top"><code>remove_button</code></td>
        <td valign="top"><i>Optional.</i> </td>
        <td valign="top"><code>Boolean</code></td>
        <td valign="top"><code>true</code></td>
    </tr>
    <tr>
        <td valign="top"><code>create</code></td>
        <td valign="top"><i>Optional. Allows the user to create a new items that aren't in the list of options.</i> </td>
        <td valign="top"><code>Boolean</code></td>
        <td valign="top"><code>true</code></td>
    </tr>
    <tr>
        <td valign="top"><code>createOnBlur</code></td>
        <td valign="top"><i>Optional. If true, when user exits the field (clicks outside of input or presses ESC) new option is created and selected (if `create`-option is enabled).</i> </td>
        <td valign="top"><code>Boolean</code></td>
        <td valign="top"><code>true</code></td>
    </tr>
    <tr>
        <td valign="top"><code>createMethod</code></td>
        <td valign="top"><i>Optional. Name of method to call after create new item</i> </td>
        <td valign="top"><code>function (label, value)</code></td>
        <td valign="top"><code>undefined</code></td>
    </tr>
            
</table>

