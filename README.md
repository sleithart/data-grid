# data-grid

A work-in-progress CSS grid layout that uses data-attributes instead of classes for columns.

[See an example here.](https://rawgit.com/sleithart/data-grid/master/index.html)


# How it works

The grid uses the role attribute to determine a grid, rows, and columns:

`
<div role="grid">
    <div role="row">
        <div role="column">
            Content goes here.
        </div>
    </div>
</div>
`

To define column width and offset, add data attributes to the column element. As the value, simply input the number of grid columns you'd like your element to span. The grid is based on a 12-column grid, but it's easy to change.

`
<div role="row">
    <div role="column" data-width="12">
        Full width column.
    </div>
</div>

<div role="row">
    <div role="column" data-width="6">
        Half width column.
    </div>
    <div role="column" data-width="6">
        Half width column.
    </div>
</div>

<div role="row">
    <div role="column" data-width="6" data-offset="3">
        Half width column with offset
    </div>
</div>
`

Your columns default to 100% width on mobile, but you can add data attributes to specify mobile width and offset.

`
<div role="row">
    <div role="column" data-width="12" data-mobile-width="6" data-mobile-offset="3">
        Full width column.
    </div>
</div>
`