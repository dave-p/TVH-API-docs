# esfilter
Functions to report on and control Elementary Stream filters.

There are separate API functions to operate on the different types of filter, but they all work in the same way. In the descriptions below the `XXX` in the function name can be replaced with `video`, `audio`, `teletext`, `subtit` (subtitle), `ca` or `other` as required.
## esfilter/XXX/class
Lists the descriptions, options and defaults for configuring the chosen type of filter, ie Configuration -> Stream -> Stream Filters -> {chosen type} -> Add.
## esfilter/XXX/grid
Returns the parameters of the defined filters of the chosen type. The usual selection options are available, see [Grid Parameters](Description.md#grid-parameters)
## esfilter/XXX/create
Creates a new filter of the chosen type.
- `conf` A JSON object describing the filter.
