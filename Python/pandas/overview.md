## Core Data Structures

| Code | Description |
|------|-------------|
| `pd.Series(data=None, index=None, dtype=None, name=None, copy=False)` | Creates a one-dimensional labeled array. `data` can be a list, numpy array, or scalar. |
| `pd.DataFrame(data=None, index=None, columns=None, dtype=None, copy=False)` | Creates a two-dimensional labeled data structure with columns of potentially different types. |
| `pd.Index(data=None, dtype=None, copy=False, name=None)` | Creates an immutable sequence used for labeling and aligning pandas data structures. |
| `pd.RangeIndex(start=0, stop=None, step=1, dtype=None, copy=False, name=None)` | Creates an index implementing a monotonic integer range. |
| `pd.MultiIndex.from_tuples(tuples, sortorder=None, names=None)` | Creates a MultiIndex from a list of tuples. |
| `pd.MultiIndex.from_arrays(arrays, sortorder=None, names=None)` | Creates a MultiIndex from a list of arrays. |
| `pd.MultiIndex.from_product(iterables, sortorder=0, names=None)` | Creates a MultiIndex from the Cartesian product of input iterables. |
| `pd.Categorical(values, categories=None, ordered=False)` | Creates a categorical data type for strings or numbers with a fixed set of possible values. |
| `pd.CategoricalIndex(categories=None, ordered=False, dtype=None)` | Creates an index of categorical data. |
| `pd.IntervalIndex.from_tuples(tuples, closed=None, name=None)` | Creates an IntervalIndex from a list of tuples. |
| `pd.IntervalIndex.from_breaks(breaks, closed=None, name=None)` | Creates an IntervalIndex from a list of breaks. |
| `pd.DatetimeIndex(data, dtype=None, copy=False, freq=None, tz=None, normalize=False, closed=None, name=None)` | Creates a DatetimeIndex for datetime64 data. |
| `pd.TimedeltaIndex(data, dtype=None, copy=False, freq=None, name=None)` | Creates a TimedeltaIndex for timedelta64 data. |
| `pd.PeriodIndex(data, dtype=None, copy=False, freq=None, name=None)` | Creates a PeriodIndex for period data. |
| `pd.SparseDtype(dtype, fill_value=0)` | Creates a sparse dtype for sparse arrays. |

---

## Input and Output

| Code | Description |
|------|-------------|
| `pd.read_csv(filepath_or_buffer, sep=',', delimiter=None, header='infer', names=None, index_col=None, usecols=None, dtype=None, engine=None, converters=None, true_values=None, false_values=None, skipinitialspace=False, skiprows=None, skipfooter=0, nrows=None, na_values=None, keep_default_na=True, na_filter=True, verbose=False, skip_blank_lines=True, parse_dates=False, infer_datetime_format=False, dayfirst=False, date_format=None, cache_dates=True, iterator=False, chunksize=None, compression='infer', thousands=None, decimal='.', lineterminator=None, quotechar='"', quoting=0, doublequote=True, escapechar=None, comment=None, encoding=None, dialect=None, on_bad_lines='error', delim_whitespace=False, low_memory=True, memory_map=False, float_precision=None, storage_options=None, dtype_backend='numpy_nullable')` | Reads a comma-separated values (csv) file into a DataFrame. |
| `pd.read_excel(io, sheet_name=0, header=0, names=None, index_col=None, usecols=None, squeeze=None, dtype=None, engine=None, converters=None, true_values=None, false_values=None, skiprows=None, nrows=None, na_values=None, keep_default_na=True, na_filter=True, verbose=False, parse_dates=False, date_parser=None, thousands=None, decimal='.', comment=None, skipfooter=0, convert_float=None, mangle_dupe_cols=True, storage_options=None, nrows=None, engine_kwargs=None)` | Reads an Excel file into a DataFrame. |
| `pd.read_sql(sql, con, index_col=None, coerce_float=True, params=None, parse_dates=None, columns=None, chunksize=None)` | Reads SQL query or database table into a DataFrame. |
| `pd.read_sql_query(sql, con, index_col=None, coerce_float=True, params=None, parse_dates=None, chunksize=None)` | Reads SQL query into a DataFrame. |
| `pd.read_sql_table(table_name, con, index_col=None, coerce_float=True, parse_dates=None, columns=None, chunksize=None)` | Reads SQL database table into a DataFrame. |
| `pd.read_json(path_or_buffer, orient=None, typ='frame', dtype=None, convert_axes=None, convert_dates=True, keep_default_dates=True, precise_float=False, date_unit=None, encoding=None, lines=False, chunksize=None, compression='infer', nrows=None, storage_options=None)` | Reads a JSON file into a DataFrame. |
| `pd.read_html(io, match='.*', flavor=None, header=None, index_col=None, skiprows=None, attrs=None, parse_dates=False, thousands=',', encoding=None, decimal='.', converters=None, dtype=None, display_max_columns=None, skip_blank_lines=True, comment=None, storage_options=None, lxml_attrs=None, nrows=None)` | Reads HTML tables into a list of DataFrame objects. |
| `pd.read_parquet(path, engine='auto', columns=None, storage_options=None, use_nullable_dtypes=False, **kwargs)` | Reads a parquet file into a DataFrame. |
| `pd.read_feather(path, columns=None, use_nullable_dtypes=False, dtype_backend='numpy_nullable', **kwargs)` | Reads a feather-format file into a DataFrame. |
| `pd.read_pickle(filepath_or_buffer, compression='infer', storage_options=None)` | Reads a pickled pandas object (DataFrame, Series, etc.) from a file. |
| `pd.read_orc(path, columns=None, storage_options=None, **kwargs)` | Reads an ORC file into a DataFrame. |
| `pd.read_table(filepath_or_buffer, sep='\t', header='infer', names=None, index_col=None, usecols=None, dtype=None, engine=None, converters=None, true_values=None, false_values=None, skipinitialspace=False, skiprows=None, skipfooter=0, nrows=None, na_values=None, keep_default_na=True, na_filter=True, verbose=False, skip_blank_lines=True, parse_dates=False, infer_datetime_format=False, dayfirst=False, date_format=None, iterator=False, chunksize=None, compression='infer', thousands=None, decimal='.', lineterminator=None, quotechar='"', quoting=0, doublequote=True, escapechar=None, comment=None, encoding=None, dialect=None, on_bad_lines='error', delim_whitespace=False, low_memory=True, memory_map=False, float_precision=None, storage_options=None)` | Reads a table-separated file into a DataFrame. |
| `pd.read_fwf(filepath_or_buffer, colspecs=None, widths=None, header='infer', index_col=None, names=None, skiprows=None, skip_blank_lines=True, skipfooter=0, nrows=None, na_values=None, keep_default_na=True, na_filter=True, verbose=False, converters=None, dtype=None, usecols=None, iterator=False, chunksize=None, compression='infer', encoding=None, dialect=None, on_bad_lines='error', delim_whitespace=False, low_memory=True, memory_map=False, float_precision=None, storage_options=None)` | Reads a fixed-width formatted file into a DataFrame. |
| `pd.read_clipboard(sep=',', header='infer', index_col=None, dtype=None, converters=None, true_values=None, false_values=None, skipinitialspace=False, skiprows=None, skipfooter=0, nrows=None, na_values=None, keep_default_na=True, na_filter=True, verbose=False, parse_dates=False, thousands=None, decimal='.', lineterminator=None, quotechar='"', quoting=0, doublequote=True, escapechar=None, comment=None, encoding=None, dialect=None, on_bad_lines='error', delim_whitespace=False, low_memory=True)` | Reads clipboard data into a DataFrame. |
| `df.to_csv(path_or_buf=None, sep=',', na_rep='', float_format=None, columns=None, header=True, index=True, index_label=None, startrow=0, endrow=None, na_rep=None, format=None, date_format=None, doublequote=True, escapechar=None, decimal='.', lineterminator=None, quotechar='"', quoting=None, compression='infer', storage_options=None, mode='w')` | Writes DataFrame to a comma-separated values (csv) file. |
| `df.to_excel(excel_writer, sheet_name='Sheet1', na_rep='', float_format=None, columns=None, header=True, index=True, index_label=None, startrow=0, startcol=0, engine=None, merge_cells=True, inf_rep='inf', freeze_panes=None, storage_options=None, if_sheet_exists=None)` | Writes DataFrame to an Excel file. |
| `df.to_sql(name, con, if_exists='fail', index=True, index_label=None, schema=None, if_exists='fail', dtype=None, method=None, chunksize=None, type=None)` | Writes DataFrame to a SQL database table. |
| `df.to_json(path_or_buf=None, orient=None, date_format=None, double_precision=10, force_ascii=True, date_unit='ms', default_handler=None, indent=None, storage_options=None, mode='w', engine='ujson', compression='infer', index=True, lines=False)` | Writes DataFrame to a JSON file. |
| `df.to_parquet(path, engine='auto', compression='snappy', index=None, storage_options=None, **kwargs)` | Writes DataFrame to a parquet file. |
| `df.to_pickle(path, compression='infer', storage_options=None, protocol=5)` | Writes DataFrame to a pickled file. |
| `df.to_html(buf=None, columns=None, col_space=None, header=True, index=True, na_rep='NaN', format=None, float_format=None, sparsify=None, index_names=True, justify=None, max_rows=None, max_cols=None, show_dimensions=False, decimal='.', bold_rows=True, classes=None, escape=True, border=1, table_id=None, render_links=False, encoding=None, local_css_file=None, storage_options=None)` | Writes DataFrame to an HTML file. |
| `df.to_latex(buf=None, columns=None, header=True, index=True, na_rep='NaN', float_format=None, sparsify=None, index_names=True, justify=None, max_rows=None, max_cols=None, show_dimensions=False, decimal='.', column_format=None, caption=None, label=None, position=None, multirow=None, multicolumn=None, multicolumn_format=None, escape=None, encoding=None, local_css_file=None)` | Writes DataFrame to a LaTeX file. |
| `df.to_markdown(buf=None, mode='wt', index=True, storage_options=None, tablefmt='grid')` | Writes DataFrame to a Markdown-formatted string. |
| `df.to_string(buf=None, columns=None, col_space=None, header=True, index=True, na_rep='NaN', format=None, float_format=None, sparsify=None, index_names=True, justify=None, max_rows=None, max_cols=None, show_dimensions=False, decimal='.', line_width=None)` | Writes DataFrame to a formatted string. |
| `df.to_dict(orient='dict', into=dict)` | Converts DataFrame to a dictionary. |
| `df.to_numpy(dtype=None, na_value=np.nan, copy=False)` | Converts DataFrame to a NumPy array. |
| `df.to_records(index=True, column_dtypes=None, index_dtypes=None)` | Converts DataFrame to a NumPy record array. |

---

## Data Selection and Indexing

| Code | Description |
|------|-------------|
| `df.loc[indexer]` | Accesses a group of rows and columns by label(s) or a boolean array. |
| `df.iloc[indexer]` | Accesses a group of rows and columns by integer position(s). |
| `df.at[index, column]` | Accesses a single value by row/column label. Similar to `loc` but for scalar access. |
| `df.iat[index, column]` | Accesses a single value by row/column position. Similar to `iloc` but for scalar access. |
| `df.head(n=5)` | Returns the first n rows of the DataFrame. |
| `df.tail(n=5)` | Returns the last n rows of the DataFrame. |
| `df.sample(n=None, frac=None, replace=False, weights=None, random_state=None, axis=None)` | Returns a random sample of items from the DataFrame. |
| `df.nsmallest(n, columns, ascending=True)` | Returns the first n rows ordered by the specified columns in ascending order. |
| `df.nlargest(n, columns, ascending=True)` | Returns the first n rows ordered by the specified columns in descending order. |
| `df.filter(items=None, like=None, regex=None, axis=None)` | Filters columns or rows based on specified criteria. |
| `df.where(cond, other=np.nan, inplace=False, axis=None, level=None)` | Replaces values where the condition is False with the specified value. |
| `df.mask(cond, other=np.nan, inplace=False, axis=None, level=None)` | Replaces values where the condition is True with the specified value. |
| `df.query(expr, engine='python', local_dict=None, resolver=None)` | Queries the DataFrame using a boolean expression. |
| `df.xs(key, axis=0, level=None, drop_level=True)` | Returns a cross-section (row or column) of the DataFrame. |
| `df.get(key, default=None)` | Gets a column or row from the DataFrame. |
| `df.__getitem__(key)` | Retrieves a column or slice of columns from the DataFrame. |
| `df.__setitem__(key, value)` | Sets a column in the DataFrame. |

---
## Data Cleaning

| Code | Description |
|------|-------------|
| `df.drop(labels=None, axis=0, index=None, columns=None, level=None, inplace=False, errors='raise')` | Drops specified labels from rows or columns. |
| `df.drop_duplicates(subset=None, keep='first', inplace=False, ignore_index=False)` | Drops duplicate rows. |
| `df.duplicated(subset=None, keep='first')` | Returns a boolean Series indicating duplicate rows. |
| `df.fillna(value=None, method=None, axis=None, inplace=False, limit=None, downcast=None)` | Fills missing values with the specified value or method. |
| `df.dropna(axis=0, how='any', thresh=None, subset=None, inplace=False)` | Drops rows or columns with missing values. |
| `df.interpolate(method='linear', axis=0, limit=None, inplace=False, limit_direction='forward', limit_area=None, downcast=None, **kwargs)` | Interpolates missing values. |
| `df.isna()` | Detects missing values. Returns a DataFrame of boolean values. |
| `df.isnull()` | Alias for `isna()`. |
| `df.notna()` | Detects non-missing values. Returns a DataFrame of boolean values. |
| `df.notnull()` | Alias for `notna()`. |
| `df.replace(to_replace=None, value=None, inplace=False, limit=None, regex=False, method='pad')` | Replaces values in the DataFrame. |
| `df.update(other, join='left', overwrite=True, filter_func=None, errors='raise')` | Modifies the DataFrame in place using non-NA values from another DataFrame. |
| `df.astype(dtype, copy=True, errors='raise')` | Casts a pandas object to a specified dtype. |
| `df.convert_dtypes(infer_objects=False, convert_string=False, convert_integer=False, convert_boolean=False, convert_floating=False, potential_column=None, force=False)` | Converts columns to the best possible dtypes. |
| `df.infer_objects(copy=False)` | Attempts to infer better dtypes for object columns. |
| `df.copy(deep=True)` | Creates a copy of the DataFrame. |
| `df.reset_index(drop=False, inplace=False, col_level=0, col_fill='')` | Resets the index of the DataFrame. |
| `df.set_index(keys, drop=True, append=False, inplace=False, verify_integrity=False)` | Sets the DataFrame index using one or more columns. |
| `df.reindex(index=None, columns=None, axis=None, method=None, copy=True, level=None, fill_value=np.nan, limit=None, tolerance=None)` | Conforms the DataFrame to a new index with optional filling logic. |
| `df.rename(mapper=None, index=None, columns=None, axis=0, copy=True, inplace=False, level=None, errors='ignore')` | Renames the DataFrame index or columns. |
| `df.rename_axis(mapper=None, index=None, columns=None, axis=0, copy=True, inplace=False)` | Renames the DataFrame index or columns axis. |

---
## Data Transformation

| Code | Description |
|------|-------------|
| `df.apply(func, axis=0, raw=False, result_type=None, args=(), **kwargs)` | Applies a function along an axis of the DataFrame. |
| `df.applymap(func)` | Applies a function element-wise across the entire DataFrame. |
| `df.map(func, na_action=None)` | Applies a function element-wise to each Series in the DataFrame. |
| `df.transform(func, axis=0, *args, **kwargs)` | Calls a function on a DataFrame and returns a DataFrame with the same shape. |
| `df.agg(func=None, axis=0, *args, **kwargs)` | Aggregates using one or more operations over the specified axis. |
| `df.aggregate(func=None, axis=0, *args, **kwargs)` | Alias for `agg()`. |
| `df.pipe(func, *args, **kwargs)` | Applies a function to the DataFrame and returns the result. |
| `df.assign(**kwargs)` | Assigns new columns to the DataFrame. |
| `df.eval(expr, inplace=False, **kwargs)` | Evaluates a string expression as a DataFrame operation. |
| `df.abs()` | Returns the absolute value of each element in the DataFrame. |
| `df.all(axis=0, bool_only=False, skipna=True, level=None)` | Returns True if all elements in the specified axis are True. |
| `df.any(axis=0, bool_only=False, skipna=True, level=None)` | Returns True if any element in the specified axis is True. |
| `df.clip(lower=None, upper=None, axis=None, inplace=False, *args, **kwargs)` | Trims values at the specified lower and upper bounds. |
| `df.cummax(axis=None, skipna=True, *args, **kwargs)` | Returns cumulative maximum over the specified axis. |
| `df.cummin(axis=None, skipna=True, *args, **kwargs)` | Returns cumulative minimum over the specified axis. |
| `df.cumprod(axis=None, skipna=True, *args, **kwargs)` | Returns cumulative product over the specified axis. |
| `df.cumsum(axis=None, skipna=True, *args, **kwargs)` | Returns cumulative sum over the specified axis. |
| `df.diff(periods=1, axis=0)` | Calculates the difference of a DataFrame element compared with another element. |
| `df.pct_change(periods=1, fill_method='pad', limit=None, freq=None, **kwargs)` | Computes percentage change between current and prior element. |
| `df.rank(axis=0, method='average', numeric_only=False, na_option='keep', ascending=True, pct=False)` | Computes numerical data ranks. |
| `df.round(decimals=0, *args, **kwargs)` | Rounds each value in the DataFrame to the specified number of decimals. |
| `df.shift(periods=1, freq=None, axis=0, fill_value=None)` | Shifts the index by the specified number of periods. |
| `df.sort_values(by, axis=0, ascending=True, inplace=False, kind='quicksort', na_position='last', ignore_index=False, key=None)` | Sorts the DataFrame by the values in the specified columns. |
| `df.sort_index(axis=0, level=None, ascending=True, inplace=False, kind='quicksort', na_position='last', sort_remaining=True, ignore_index=False, key=None)` | Sorts the DataFrame by the index. |
| `df.nsmallest(n, columns, ascending=True)` | Returns the first n rows ordered by the specified columns in ascending order. |
| `df.nlargest(n, columns, ascending=True)` | Returns the first n rows ordered by the specified columns in descending order. |

---
## Aggregation and Grouping

| Code | Description |
|------|-------------|
| `df.groupby(by=None, axis=0, level=None, as_index=True, sort=True, group_keys=True, observed=False, dropna=True)` | Groups DataFrame using a mapper or by a Series of columns. |
| `df.groupby(by).agg(func)` | Aggregates grouped data using one or more operations. |
| `df.groupby(by).aggregate(func)` | Alias for `agg()`. |
| `df.groupby(by).transform(func)` | Transforms grouped data and returns a DataFrame with the same shape. |
| `df.groupby(by).apply(func, *args, **kwargs)` | Applies a function to each group. |
| `df.groupby(by).filter(func, *args, **kwargs)` | Filters groups based on a function. |
| `df.groupby(by).first()` | Returns the first value in each group. |
| `df.groupby(by).last()` | Returns the last value in each group. |
| `df.groupby(by).sum()` | Returns the sum of values in each group. |
| `df.groupby(by).mean()` | Returns the mean of values in each group. |
| `df.groupby(by).median()` | Returns the median of values in each group. |
| `df.groupby(by).min()` | Returns the minimum of values in each group. |
| `df.groupby(by).max()` | Returns the maximum of values in each group. |
| `df.groupby(by).count()` | Returns the count of non-NA values in each group. |
| `df.groupby(by).size()` | Returns the size of each group. |
| `df.groupby(by).std()` | Returns the standard deviation of values in each group. |
| `df.groupby(by).var()` | Returns the variance of values in each group. |
| `df.groupby(by).sem()` | Returns the standard error of the mean of values in each group. |
| `df.groupby(by).describe()` | Generates descriptive statistics for each group. |
| `df.groupby(by).head(n=5)` | Returns the first n rows of each group. |
| `df.groupby(by).tail(n=5)` | Returns the last n rows of each group. |
| `df.groupby(by).nth(n, column=None)` | Returns the nth row of each group. |
| `df.pivot(index=None, columns=None, values=None)` | Returns a reshaped DataFrame based on column values. |
| `df.pivot_table(values=None, index=None, columns=None, aggfunc='mean', fill_value=None, margins=False, dropna=True, margins_name='All', observed=False, sort=True)` | Creates a pivot table as a DataFrame. |
| `df.melt(id_vars=None, value_vars=None, var_name=None, value_name='value', col_level=None, ignore_index=True)` | Unpivots a DataFrame from wide format to long format. |
| `df.stack(future_stack=False, dropna=True, sort=True)` | Stacks the prescribed level(s) from columns to index. |
| `df.unstack(level=-1, fill_value=None)` | Unstacks the prescribed level(s) from index to columns. |
| `pd.crosstab(index, columns, values=None, rownames=None, colnames=None, aggfunc=None, margins=False, margins_name='All', dropna=True, normalize=False)` | Computes a simple cross-tabulation of two or more factors. |
| `pd.cut(x, bins, right=True, labels=None, retbins=False, include_lowest=False, duplicates='raise', ordered=False)` | Bins values into discrete intervals. |
| `pd.qcut(x, q, labels=None, retbins=False, duplicates='raise', axis=0)` | Quantile-based discretization function. |
| `pd.merge(left, right, how='inner', on=None, left_on=None, right_on=None, left_index=False, right_index=False, sort=True, suffixes=('_x', '_y'), copy=True, indicator=False, validate=None)` | Merges DataFrame or named Series objects with database-style joins. |
| `pd.concat(objs, axis=0, join='outer', ignore_index=False, keys=None, levels=None, names=None, verify_integrity=False, sort=False, copy=True)` | Concatenates pandas objects along a particular axis. |
| `pd.concat([df1, df2], axis=1)` | Concatenates DataFrames horizontally (column-wise). |
| `pd.concat([df1, df2], axis=0)` | Concatenates DataFrames vertically (row-wise). |
| `df.join(other, on=None, how='left', lsuffix='_left', rsuffix='_right', sort=False)` | Joins columns of another DataFrame. |
| `df.append(other, ignore_index=False, verify_integrity=False, sort=False)` | Appends rows of other to the end of the DataFrame. |
| `pd.merge_ordered(left, right, on=None, left_on=None, right_on=None, left_by=None, right_by=None, fill_method=None, suffixes=('_x', '_y'))` | Performs a merge for ordered data. |
| `pd.merge_asof(left, right, on=None, left_on=None, right_on=None, left_index=True, right_index=True, by=None, left_by=None, right_by=None, suffixes=('_x', '_y'), tolerance=None, direction='backward')` | Performs an asof merge for ordered data. |

---
## Time Series

| Code | Description |
|------|-------------|
| `pd.date_range(start=None, end=None, periods=None, freq=None, tz=None, normalize=False, name=None, closed=None, **kwargs)` | Generates a date range. |
| `pd.period_range(start=None, end=None, periods=None, freq=None, name=None)` | Generates a period range. |
| `pd.timedelta_range(start=None, end=None, periods=None, freq=None, name=None, closed=None)` | Generates a timedelta range. |
| `pd.to_datetime(arg, errors='raise', dayfirst=False, yearfirst=False, utc=False, format=None, exact=True, unit=None, infer_datetime_format=False, origin='unix', cache=True)` | Converts argument to datetime. |
| `pd.to_timedelta(arg, unit=None, errors='raise')` | Converts argument to timedelta. |
| `pd.Timestamp(ts_input=None, year=None, month=None, day=None, hour=None, minute=None, second=None, millisecond=None, microsecond=None, nanosecond=None, tz=None, utc=False, normalize=False)` | Creates a Timestamp object. |
| `pd.Timedelta(value=0, unit=None, attrs=None)` | Creates a Timedelta object. |
| `pd.Period(year=None, month=None, day=None, hour=None, minute=None, second=None, quarter=None, week=None, ordinal=None, freq=None)` | Creates a Period object. |
| `pd.NaT` | Represents a missing datetime value. |
| `pd.DatetimeTZDtype(unit=None, tz=None)` | Creates a datetime with timezone dtype. |
| `pd.TimedeltaIndex` | Immutable sequence of timedelta64 data. |
| `pd.PeriodIndex` | Immutable sequence of period data. |
| `df.resample(rule, axis=0, closed=None, label=None, convention='start', origin='start_day', offset=None, on=None, level=None, kind=None, fill_method=None)` | Resamples the DataFrame to a specified frequency. |
| `df.rolling(window, min_periods=None, center=False, win_type=None, on=None, axis=0, closed=None, step=None, method='table')` | Provides rolling window calculations. |
| `df.expanding(min_periods=1, method='table', axis=0)` | Provides expanding window calculations. |
| `df.ewm(com=None, span=None, halflife=None, alpha=None, min_periods=0, adjust=True, ignore_na=False, axis=0, times=None, method='table')` | Provides exponential weighted window calculations. |
| `df.shift(periods=1, freq=None, axis=0, fill_value=None)` | Shifts the index by the specified number of periods. |
| `df.diff(periods=1, axis=0)` | Calculates the difference of a DataFrame element compared with another element. |
| `df.pct_change(periods=1, fill_method='pad', limit=None, freq=None)` | Computes percentage change between current and prior element. |

---
## String Operations

| Code | Description |
|------|-------------|
| `s.str` | Accessor for string methods on Series or Index with string dtype. |
| `s.str.capitalize()` | Converts strings to capitalize case. |
| `s.str.casefold()` | Converts strings to casefolded case. |
| `s.str.cat(others=None, sep=None, na_rep='')` | Concatenates strings with the specified separator. |
| `s.str.center(width, fillchar=' ')` | Centers strings with the specified width and fill character. |
| `s.str.contains(pat, case=True, flags=0, na=None, regex=True)` | Checks if each string contains the specified pattern. |
| `s.str.count(pat, flags=0, case=True)` | Counts occurrences of the specified pattern. |
| `s.str.decode(encoding='utf-8', errors='strict')` | Decodes strings using the specified encoding. |
| `s.str.encode(encoding='utf-8', errors='strict')` | Encodes strings using the specified encoding. |
| `s.str.endswith(pat, na=None)` | Checks if each string ends with the specified pattern. |
| `s.str.extract(pat, flags=0, expand=True)` | Extracts the first match of the specified pattern. |
| `s.str.extractall(pat, flags=0)` | Extracts all matches of the specified pattern. |
| `s.str.find(sub, start=0, end=None)` | Returns the lowest index where the substring is found. |
| `s.str.findall(pat, flags=0)` | Finds all occurrences of the specified pattern. |
| `s.str.fullmatch(pat, flags=0, case=True)` | Checks if each string fully matches the specified pattern. |
| `s.str.get(i)` | Extracts the i-th element from each string. |
| `s.str.index(sub, start=0, end=None)` | Returns the index where the substring is found. |
| `s.str.isalnum()` | Checks if all characters are alphanumeric. |
| `s.str.isalpha()` | Checks if all characters are alphabetic. |
| `s.str.isdecimal()` | Checks if all characters are decimal. |
| `s.str.isdigit()` | Checks if all characters are digits. |
| `s.str.isidentifier()` | Checks if the string is a valid Python identifier. |
| `s.str.islower()` | Checks if all characters are lowercase. |
| `s.str.isnumeric()` | Checks if all characters are numeric. |
| `s.str.isprintable()` | Checks if all characters are printable. |
| `s.str.isspace()` | Checks if all characters are whitespace. |
| `s.str.istitle()` | Checks if the string is titlecase. |
| `s.str.isupper()` | Checks if all characters are uppercase. |
| `s.str.join(sep)` | Joins strings in the Series with the specified separator. |
| `s.str.ljust(width, fillchar=' ')` | Left-justifies strings with the specified width and fill character. |
| `s.str.lower()` | Converts strings to lowercase. |
| `s.str.lstrip(chars=None)` | Removes leading whitespace or specified characters. |
| `s.str.match(pat, flags=0, na=None, case=True)` | Checks if each string matches the specified pattern at the beginning. |
| `s.str.normalize(form)` | Normalizes strings to the specified form. |
| `s.str.pad(width, side='left', fillchar=' ')` | Pads strings with the specified width, side, and fill character. |
| `s.str.partition(sep, expand=True)` | Partitions each string at the first occurrence of the separator. |
| `s.str.repeat(repeats, axis=None)` | Repeats each string the specified number of times. |
| `s.str.replace(pat, repl, n=-1, case=True, flags=0, regex=True)` | Replaces occurrences of the specified pattern with the replacement. |
| `s.str.rfind(sub, start=0, end=None)` | Returns the highest index where the substring is found. |
| `s.str.rindex(sub, start=0, end=None)` | Returns the highest index where the substring is found. |
| `s.str.rjust(width, fillchar=' ')` | Right-justifies strings with the specified width and fill character. |
| `s.str.rpartition(sep, expand=True)` | Partitions each string at the last occurrence of the separator. |
| `s.str.rstrip(chars=None)` | Removes trailing whitespace or specified characters. |
| `s.str.slice(start=None, stop=None, step=None)` | Slices each string from start to stop with the specified step. |
| `s.str.slice_replace(start=None, stop=None, repl=None)` | Replaces the slice of each string with the replacement. |
| `s.str.split(pat=None, n=-1, expand=False)` | Splits each string at the specified separator. |
| `s.str.rsplit(pat=None, n=-1, expand=False)` | Splits each string at the specified separator, starting from the end. |
| `s.str.startswith(pat, na=None)` | Checks if each string starts with the specified pattern. |
| `s.str.strip(chars=None)` | Removes leading and trailing whitespace or specified characters. |
| `s.str.swapcase()` | Swaps the case of each character. |
| `s.str.title()` | Converts strings to titlecase. |
| `s.str.translate(table)` | Translates each string using the specified translation table. |
| `s.str.upper()` | Converts strings to uppercase. |
| `s.str.wrap(width, expand_tabs=True, replace_whitespace=True, max_lines=None, break_long_words=True, break_on_hyphens=False)` | Wraps strings to the specified width. |
| `s.str.zfill(width)` | Pads strings with zeros on the left to the specified width. |

---
## Missing Data Handling

| Code | Description |
|------|-------------|
| `df.isna()` | Detects missing values. Returns a DataFrame of boolean values. |
| `df.isnull()` | Alias for `isna()`. |
| `df.notna()` | Detects non-missing values. Returns a DataFrame of boolean values. |
| `df.notnull()` | Alias for `notna()`. |
| `df.dropna(axis=0, how='any', thresh=None, subset=None, inplace=False)` | Drops rows or columns with missing values. |
| `df.fillna(value=None, method=None, axis=None, inplace=False, limit=None, downcast=None)` | Fills missing values with the specified value or method. |
| `df.interpolate(method='linear', axis=0, limit=None, inplace=False, limit_direction='forward', limit_area=None, downcast=None, **kwargs)` | Interpolates missing values. |
| `pd.isna(obj)` | Detects missing values in a pandas object. |
| `pd.isnull(obj)` | Alias for `isna()`. |
| `pd.notna(obj)` | Detects non-missing values in a pandas object. |
| `pd.notnull(obj)` | Alias for `notna()`. |
| `pd.NA` | Represents a missing value in pandas. |
| `pd.NAType` | Type for `pd.NA`. |
| `pd.isna(obj)` | Checks for missing values in an object. |
| `pd.NA` | Missing value indicator in pandas. |
| `df.ffill(axis=None, inplace=False, limit=None, downcast=None)` | Fills missing values by propagating the last valid observation forward. |
| `df.bfill(axis=None, inplace=False, limit=None, downcast=None)` | Fills missing values by using the next valid observation. |

---
## Type Conversion

| Code | Description |
|------|-------------|
| `df.astype(dtype, copy=True, errors='raise')` | Casts a pandas object to a specified dtype. |
| `df.convert_dtypes(infer_objects=False, convert_string=False, convert_integer=False, convert_boolean=False, convert_floating=False, potential_column=None, force=False)` | Converts columns to the best possible dtypes. |
| `pd.to_numeric(arg, errors='raise', downcast=None)` | Converts argument to a numeric type. |
| `pd.to_datetime(arg, errors='raise', dayfirst=False, yearfirst=False, utc=False, format=None, exact=True, unit=None, infer_datetime_format=False, origin='unix', cache=True)` | Converts argument to datetime. |
| `pd.to_timedelta(arg, unit=None, errors='raise')` | Converts argument to timedelta. |
| `pd.to_numeric(arg, errors='raise', downcast=None)` | Converts argument to a numeric type. |
| `pd.to_categorical(arg, categories=None, ordered=False)` | Converts argument to a categorical type. |
| `s.astype(dtype, copy=True, errors='raise')` | Casts a Series to a specified dtype. |
| `s.to_frame(name=None)` | Converts a Series to a DataFrame. |
| `df.to_dict(orient='dict', into=dict)` | Converts DataFrame to a dictionary. |
| `df.to_numpy(dtype=None, na_value=np.nan, copy=False)` | Converts DataFrame to a NumPy array. |
| `df.to_records(index=True, column_dtypes=None, index_dtypes=None)` | Converts DataFrame to a NumPy record array. |
| `s.to_list()` | Converts a Series to a list. |
| `s.to_numpy(dtype=None, na_value=np.nan, copy=False)` | Converts a Series to a NumPy array. |
| `pd.get_dummies(data, prefix=None, prefix_sep='_', dummy_na=False, columns=None, sparse=False, drop_first=False, dtype=None)` | Converts categorical variables into dummy/indicator variables. |

---
## Data Inspection

| Code | Description |
|------|-------------|
| `df.info(verbose=None, buffer=None, max_cols=None, max_rows=None, show_counts=False, memory_usage=True, null_counts=False)` | Prints a concise summary of a DataFrame. |
| `df.describe(percentiles=None, include=None, exclude=None, datetime_is_numeric=False)` | Generates descriptive statistics. |
| `df.head(n=5)` | Returns the first n rows of the DataFrame. |
| `df.tail(n=5)` | Returns the last n rows of the DataFrame. |
| `df.shape` | Returns a tuple representing the dimensionality of the DataFrame. |
| `df.size` | Returns the number of elements in the DataFrame. |
| `df.ndim` | Returns the number of dimensions of the DataFrame. |
| `df.columns` | Returns the column labels of the DataFrame. |
| `df.index` | Returns the index (row labels) of the DataFrame. |
| `df.dtypes` | Returns the data types of the DataFrame columns. |
| `df.axes` | Returns a list of the DataFrame axes. |
| `df.values` | Returns the underlying data as a NumPy array. |
| `df.T` | Returns the transpose of the DataFrame. |
| `df.memory_usage(index=True, deep=False)` | Returns the memory usage of each column. |
| `df.empty` | Returns True if the DataFrame is empty. |
| `df.count(non_unique=False)` | Counts non-NA cells for each column or row. |
| `df.nunique(axis=0, dropna=True)` | Returns the number of unique values for each column or row. |
| `df.value_counts(subset=None, normalize=False, sort=True, ascending=False, bins=None, dropna=True)` | Returns a Series containing counts of unique values. |
| `df.nsmallest(n, columns, ascending=True)` | Returns the first n rows ordered by the specified columns in ascending order. |
| `df.nlargest(n, columns, ascending=True)` | Returns the first n rows ordered by the specified columns in descending order. |
| `df.sample(n=None, frac=None, replace=False, weights=None, random_state=None, axis=None)` | Returns a random sample of items from the DataFrame. |
| `df.corr(method='pearson', min_periods=1, numeric_only=False)` | Computes pairwise correlation of columns, excluding NA/null values. |
| `df.cov(min_periods=1, numeric_only=False)` | Computes pairwise covariance of columns, excluding NA/null values. |
| `df.skew(axis=0, skipna=True, numeric_only=False)` | Returns the skewness of the DataFrame. |
| `df.kurt(axis=0, skipna=True, numeric_only=False)` | Returns the kurtosis of the DataFrame. |
| `df.quantile(q=0.5, axis=0, numeric_only=False, interpolation='linear')` | Returns the specified quantile values. |
| `df.cumsum(axis=None, skipna=True, *args, **kwargs)` | Returns cumulative sum over the specified axis. |
| `df.cumprod(axis=None, skipna=True, *args, **kwargs)` | Returns cumulative product over the specified axis. |
| `df.cummax(axis=None, skipna=True, *args, **kwargs)` | Returns cumulative maximum over the specified axis. |
| `df.cummin(axis=None, skipna=True, *args, **kwargs)` | Returns cumulative minimum over the specified axis. |

---
## Statistical Functions

| Code | Description |
|------|-------------|
| `df.sum(axis=None, skipna=True, numeric_only=False, min_count=0)` | Returns the sum of values over the specified axis. |
| `df.mean(axis=None, skipna=True, numeric_only=False)` | Returns the mean of values over the specified axis. |
| `df.median(axis=None, skipna=True, numeric_only=False)` | Returns the median of values over the specified axis. |
| `df.min(axis=None, skipna=True, numeric_only=False)` | Returns the minimum of values over the specified axis. |
| `df.max(axis=None, skipna=True, numeric_only=False)` | Returns the maximum of values over the specified axis. |
| `df.std(axis=None, skipna=True, ddof=1, numeric_only=False)` | Returns the standard deviation of values over the specified axis. |
| `df.var(axis=None, skipna=True, ddof=1, numeric_only=False)` | Returns the variance of values over the specified axis. |
| `df.sem(axis=None, skipna=True, ddof=1, numeric_only=False)` | Returns the standard error of the mean of values over the specified axis. |
| `df.count(non_unique=False)` | Counts non-NA cells for each column or row. |
| `df.nunique(axis=0, dropna=True)` | Returns the number of unique values for each column or row. |
| `df.describe(percentiles=None, include=None, exclude=None, datetime_is_numeric=False)` | Generates descriptive statistics. |
| `df.quantile(q=0.5, axis=0, numeric_only=False, interpolation='linear')` | Returns the specified quantile values. |
| `df.corr(method='pearson', min_periods=1, numeric_only=False)` | Computes pairwise correlation of columns, excluding NA/null values. |
| `df.cov(min_periods=1, numeric_only=False)` | Computes pairwise covariance of columns, excluding NA/null values. |
| `df.skew(axis=0, skipna=True, numeric_only=False)` | Returns the skewness of the DataFrame. |
| `df.kurt(axis=0, skipna=True, numeric_only=False)` | Returns the kurtosis of the DataFrame. |
| `df.abs()` | Returns the absolute value of each element in the DataFrame. |
| `df.all(axis=0, bool_only=False, skipna=True, level=None)` | Returns True if all elements in the specified axis are True. |
| `df.any(axis=0, bool_only=False, skipna=True, level=None)` | Returns True if any element in the specified axis is True. |

---
## Window Functions

| Code | Description |
|------|-------------|
| `df.rolling(window, min_periods=None, center=False, win_type=None, on=None, axis=0, closed=None, step=None, method='table')` | Provides rolling window calculations. |
| `Rolling.mean()` | Returns the rolling mean. |
| `Rolling.sum()` | Returns the rolling sum. |
| `Rolling.min()` | Returns the rolling minimum. |
| `Rolling.max()` | Returns the rolling maximum. |
| `Rolling.count()` | Returns the rolling count of non-NA values. |
| `Rolling.std()` | Returns the rolling standard deviation. |
| `Rolling.var()` | Returns the rolling variance. |
| `Rolling.median()` | Returns the rolling median. |
| `Rolling.apply(func, raw=False, args=(), kwargs={})` | Applies a function to the rolling window. |
| `Rolling.quantile(q, interpolation='linear')` | Returns the rolling quantile. |
| `Rolling.skew()` | Returns the rolling skewness. |
| `Rolling.kurt()` | Returns the rolling kurtosis. |
| `df.expanding(min_periods=1, method='table', axis=0)` | Provides expanding window calculations. |
| `Expanding.mean()` | Returns the expanding mean. |
| `Expanding.sum()` | Returns the expanding sum. |
| `Expanding.min()` | Returns the expanding minimum. |
| `Expanding.max()` | Returns the expanding maximum. |
| `Expanding.count()` | Returns the expanding count of non-NA values. |
| `Expanding.std()` | Returns the expanding standard deviation. |
| `Expanding.var()` | Returns the expanding variance. |
| `Expanding.median()` | Returns the expanding median. |
| `Expanding.apply(func, raw=False, args=(), kwargs={})` | Applies a function to the expanding window. |
| `df.ewm(com=None, span=None, halflife=None, alpha=None, min_periods=0, adjust=True, ignore_na=False, axis=0, times=None, method='table')` | Provides exponential weighted window calculations. |
| `ExponentialMovingWindow.mean()` | Returns the exponential weighted moving mean. |
| `ExponentialMovingWindow.sum()` | Returns the exponential weighted moving sum. |
| `ExponentialMovingWindow.std()` | Returns the exponential weighted moving standard deviation. |
| `ExponentialMovingWindow.var()` | Returns the exponential weighted moving variance. |
| `ExponentialMovingWindow.min()` | Returns the exponential weighted moving minimum. |
| `ExponentialMovingWindow.max()` | Returns the exponential weighted moving maximum. |

---
## Merging and Joining

| Code | Description |
|------|-------------|
| `pd.merge(left, right, how='inner', on=None, left_on=None, right_on=None, left_index=False, right_index=False, sort=True, suffixes=('_x', '_y'), copy=True, indicator=False, validate=None)` | Merges DataFrame or named Series objects with database-style joins. |
| `pd.merge_ordered(left, right, on=None, left_on=None, right_on=None, left_by=None, right_by=None, fill_method=None, suffixes=('_x', '_y'))` | Performs a merge for ordered data. |
| `pd.merge_asof(left, right, on=None, left_on=None, right_on=None, left_index=True, right_index=True, by=None, left_by=None, right_by=None, suffixes=('_x', '_y'), tolerance=None, direction='backward')` | Performs an asof merge for ordered data. |
| `pd.concat(objs, axis=0, join='outer', ignore_index=False, keys=None, levels=None, names=None, verify_integrity=False, sort=False, copy=True)` | Concatenates pandas objects along a particular axis. |
| `df.join(other, on=None, how='left', lsuffix='_left', rsuffix='_right', sort=False)` | Joins columns of another DataFrame. |
| `df.append(other, ignore_index=False, verify_integrity=False, sort=False)` | Appends rows of other to the end of the DataFrame. |
| `df.combine(other, func, fill_value=None)` | Combines two DataFrames using the specified function. |
| `df.combine_first(other)` | Updates null elements with non-null values from other. |
| `df.update(other, join='left', overwrite=True, filter_func=None, errors='raise')` | Modifies the DataFrame in place using non-NA values from another DataFrame. |

---
## Reshaping

| Code | Description |
|------|-------------|
| `df.pivot(index=None, columns=None, values=None)` | Returns a reshaped DataFrame based on column values. |
| `df.pivot_table(values=None, index=None, columns=None, aggfunc='mean', fill_value=None, margins=False, dropna=True, margins_name='All', observed=False, sort=True)` | Creates a pivot table as a DataFrame. |
| `df.melt(id_vars=None, value_vars=None, var_name=None, value_name='value', col_level=None, ignore_index=True)` | Unpivots a DataFrame from wide format to long format. |
| `df.stack(future_stack=False, dropna=True, sort=True)` | Stacks the prescribed level(s) from columns to index. |
| `df.unstack(level=-1, fill_value=None)` | Unstacks the prescribed level(s) from index to columns. |
| `df.explode(column, ignore_index=False)` | Transforms each element of a list-like column to a separate row. |
| `pd.crosstab(index, columns, values=None, rownames=None, colnames=None, aggfunc=None, margins=False, margins_name='All', dropna=True, normalize=False)` | Computes a simple cross-tabulation of two or more factors. |
| `pd.wide_to_long(df, stubnames, i, j, sep, suffix)` | Converts wide format DataFrames to long format. |
| `pd.melt(df, id_vars=None, value_vars=None, var_name=None, value_name='value', col_level=None, ignore_index=True)` | Unpivots a DataFrame from wide format to long format. |
| `df.transpose(*args, copy=False)` | Transposes the DataFrame. |
| `df.T` | Returns the transpose of the DataFrame. |

---
## Categorical Data

| Code | Description |
|------|-------------|
| `pd.Categorical(values, categories=None, ordered=False)` | Creates a categorical data type for strings or numbers with a fixed set of possible values. |
| `pd.CategoricalIndex(categories=None, ordered=False, dtype=None)` | Creates an index of categorical data. |
| `pd.cut(x, bins, right=True, labels=None, retbins=False, include_lowest=False, duplicates='raise', ordered=False)` | Bins values into discrete intervals. |
| `pd.qcut(x, q, labels=None, retbins=False, duplicates='raise', axis=0)` | Quantile-based discretization function. |
| `s.astype('category')` | Converts a Series to a categorical type. |
| `df['column'].astype('category')` | Converts a DataFrame column to a categorical type. |
| `pd.Categorical.from_codes(codes, categories, ordered=False)` | Creates a Categorical from codes and categories. |
| `pd.get_dummies(data, prefix=None, prefix_sep='_', dummy_na=False, columns=None, sparse=False, drop_first=False, dtype=None)` | Converts categorical variables into dummy/indicator variables. |
| `s.cat` | Accessor for categorical Series. |
| `s.cat.categories` | Returns the categories of the categorical Series. |
| `s.cat.codes` | Returns the codes of the categorical Series. |
| `s.cat.ordered` | Returns whether the categorical Series is ordered. |
| `s.cat.rename_categories(new_categories)` | Renames the categories of the categorical Series. |
| `s.cat.reorder_categories(new_categories, ordered=None)` | Reorders the categories of the categorical Series. |
| `s.cat.add_categories(new_categories)` | Adds new categories to the categorical Series. |
| `s.cat.remove_categories(categories)` | Removes categories from the categorical Series. |
| `s.cat.remove_unused_categories()` | Removes unused categories from the categorical Series. |
| `s.cat.set_categories(new_categories, ordered=None)` | Sets the categories of the categorical Series. |

---
## Plotting

| Code | Description |
|------|-------------|
| `df.plot(x=None, y=None, kind='line', ax=None, subplots=False, sharex=None, sharey=False, layout=None, figsize=None, use_index=True, title=None, grid=None, legend=True, style=None, logx=False, logy=False, loglog=False, xticks=None, yticks=None, xlim=None, ylim=None, rot=None, fontsize=None, colormap=None, table=False, yerr=None, xerr=None, secondary_y=False, sort_columns=False, **kwds)` | Generates a plot of the DataFrame. |
| `df.plot.line(x=None, y=None, **kwargs)` | Generates a line plot. |
| `df.plot.bar(x=None, y=None, **kwargs)` | Generates a bar plot. |
| `df.plot.barh(x=None, y=None, **kwargs)` | Generates a horizontal bar plot. |
| `df.plot.hist(bins=10, **kwargs)` | Generates a histogram. |
| `df.plot.box(**kwargs)` | Generates a box plot. |
| `df.plot.kde(**kwargs)` | Generates a kernel density estimate plot. |
| `df.plot.density(**kwargs)` | Alias for `kde()`. |
| `df.plot.area(x=None, y=None, **kwargs)` | Generates an area plot. |
| `df.plot.pie(y=None, **kwargs)` | Generates a pie chart. |
| `df.plot.scatter(x, y, **kwargs)` | Generates a scatter plot. |
| `df.plot.hexbin(x, y, gridsize=10, **kwargs)` | Generates a hexbin plot. |
| `df.plot.boxplot(**kwargs)` | Generates a box plot for each column. |
| `df.hist(bins=10, **kwargs)` | Generates a histogram for each column. |
| `pd.plotting.scatter_matrix(frame, alpha=0.5, figsize=None, ax=None, grid=False, diagonal='hist', marker='.', density_kwds=None, range_padding=0.05, **kwargs)` | Generates a scatter matrix. |
| `pd.plotting.parallel_coordinates(frame, class_column, cols=None, ax=None, alpha=0.5, color=None, **kwargs)` | Generates a parallel coordinates plot. |
| `pd.plotting.radviz(frame, class_column, cols=None, ax=None, color=None, alpha=0.5, **kwargs)` | Generates a radviz plot. |
| `pd.plotting.andrews_curves(frame, class_column, cols=None, ax=None, **kwargs)` | Generates an Andrews curves plot. |
| `pd.plotting.bootstrap_plot(frame, size=50, samples=1000, color=None, **kwargs)` | Generates a bootstrap plot. |
| `pd.plotting.lag_plot(frame, lag=1, ax=None, **kwargs)` | Generates a lag plot. |
| `pd.plotting.autocorrelation_plot(frame, ax=None, **kwargs)` | Generates an autocorrelation plot. |

---
## Options and Settings

| Code | Description |
|------|-------------|
| `pd.set_option(pat, value)` | Sets the specified option. |
| `pd.get_option(pat)` | Gets the specified option. |
| `pd.reset_option(pat)` | Resets the specified option to its default value. |
| `pd.describe_option(pat, _print_desc=True)` | Describes the specified option. |
| `pd.options` | Namespace for pandas options. |
| `pd.options.display` | Namespace for display options. |
| `pd.options.display.max_columns` | Maximum number of columns to display. |
| `pd.options.display.max_rows` | Maximum number of rows to display. |
| `pd.options.display.width` | Maximum width of the display in characters. |
| `pd.options.display.precision` | Floating-point output precision. |
| `pd.options.display.float_format` | Floating-point output format. |
| `pd.options.display.max_colwidth` | Maximum width of columns to display. |
| `pd.options.display.colheader_justify` | Controls the justification of column headers. |
| `pd.options.display.show_dimensions` | Whether to display the DataFrame dimensions. |
| `pd.options.mode` | Namespace for mode options. |
| `pd.options.mode.chained_assignment` | Whether to raise an exception when chained assignment is used. |
| `pd.options.plotting` | Namespace for plotting options. |
| `pd.options.plotting.backend` | The plotting backend to use. |
| `pd.options.io` | Namespace for I/O options. |
| `pd.options.io.excel` | Namespace for Excel I/O options. |
| `pd.options.io.excel.xlsx.writer` | The Excel writer to use. |
| `pd.options.io.excel.xlsm.writer` | The Excel writer to use for xlsm files. |
| `pd.options.io.excel.xls.writer` | The Excel writer to use for xls files. |

---
## Utilities

| Code | Description |
|------|-------------|
| `pd.Series(data=None, index=None, dtype=None, name=None, copy=False)` | Creates a one-dimensional labeled array. |
| `pd.DataFrame(data=None, index=None, columns=None, dtype=None, copy=False)` | Creates a two-dimensional labeled data structure. |
| `pd.Index(data=None, dtype=None, copy=False, name=None)` | Creates an immutable sequence used for labeling. |
| `pd.to_datetime(arg, errors='raise', dayfirst=False, yearfirst=False, utc=False, format=None, exact=True, unit=None, infer_datetime_format=False, origin='unix', cache=True)` | Converts argument to datetime. |
| `pd.to_timedelta(arg, unit=None, errors='raise')` | Converts argument to timedelta. |
| `pd.to_numeric(arg, errors='raise', downcast=None)` | Converts argument to a numeric type. |
| `pd.to_categorical(arg, categories=None, ordered=False)` | Converts argument to a categorical type. |
| `pd.get_dummies(data, prefix=None, prefix_sep='_', dummy_na=False, columns=None, sparse=False, drop_first=False, dtype=None)` | Converts categorical variables into dummy/indicator variables. |
| `pd.cut(x, bins, right=True, labels=None, retbins=False, include_lowest=False, duplicates='raise', ordered=False)` | Bins values into discrete intervals. |
| `pd.qcut(x, q, labels=None, retbins=False, duplicates='raise', axis=0)` | Quantile-based discretization function. |
| `pd.merge(left, right, how='inner', on=None, left_on=None, right_on=None, left_index=False, right_index=False, sort=True, suffixes=('_x', '_y'), copy=True, indicator=False, validate=None)` | Merges DataFrame or named Series objects. |
| `pd.concat(objs, axis=0, join='outer', ignore_index=False, keys=None, levels=None, names=None, verify_integrity=False, sort=False, copy=True)` | Concatenates pandas objects. |
| `pd.isna(obj)` | Detects missing values in a pandas object. |
| `pd.isnull(obj)` | Alias for `isna()`. |
| `pd.notna(obj)` | Detects non-missing values in a pandas object. |
| `pd.notnull(obj)` | Alias for `notna()`. |
| `pd.NA` | Represents a missing value in pandas. |
| `pd.NAType` | Type for `pd.NA`. |
| `pd.NaT` | Represents a missing datetime value. |
| `pd.Timestamp(ts_input=None, year=None, month=None, day=None, hour=None, minute=None, second=None, millisecond=None, microsecond=None, nanosecond=None, tz=None, utc=False, normalize=False)` | Creates a Timestamp object. |
| `pd.Timedelta(value=0, unit=None, attrs=None)` | Creates a Timedelta object. |
| `pd.Period(year=None, month=None, day=None, hour=None, minute=None, second=None, quarter=None, week=None, ordinal=None, freq=None)` | Creates a Period object. |
| `pd.date_range(start=None, end=None, periods=None, freq=None, tz=None, normalize=False, name=None, closed=None, **kwargs)` | Generates a date range. |
| `pd.period_range(start=None, end=None, periods=None, freq=None, name=None)` | Generates a period range. |
| `pd.timedelta_range(start=None, end=None, periods=None, freq=None, name=None, closed=None)` | Generates a timedelta range. |
| `pd.IntervalIndex.from_tuples(tuples, closed=None, name=None)` | Creates an IntervalIndex from a list of tuples. |
| `pd.IntervalIndex.from_breaks(breaks, closed=None, name=None)` | Creates an IntervalIndex from a list of breaks. |