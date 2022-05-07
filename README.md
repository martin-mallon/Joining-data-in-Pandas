<h1><font color='black'>Joining data in Pandas</font></h1>

<br>

<br>

<p align="center" width="100%">
    <img width="50%" src="Joining_data_in_Pandas/Assets/inner_join_1.png">
</p>

<br>

<h3><font color='grey'>Pandas basics</font></h3>

<p>Combining data points across multiple sources is made possible using <code>merge</code>. With a common value, such as a <code>unique_id</code>, relationships can be formed between tables allowing additional data points to be retrieved. Merging data frames is a useful way to access lookup tables where data typically has a one-to-one relationship, like pulling through a user's <code>average_order_value</code> from a neighbouring table. Tables with a one-to-many relationship can be merged to pull through multiple observations, e.g. joining an accounts_table to a <code>pages_viewed</code>. The nature of the join (<code>inner/left/right/outer</code>) will impact what data is filtered and whether a merge will pull through Null values.</p>

<ul>
    <li><b><code>pd.DataFrame()</code></b> - Data frames are table structures that contain data. The function <code>csv_to_df</code> reads <code>.csv</code> files and stores the data as data frames to be used later when building merges. The data frame <code>jrny</code> contains digital journey touchpoints for each session which will be used as a primary reference.</li>
    <br>
    <li><b><code>df.merge()</code></b> - The <code>merge()</code> method updates the content of two data frames by merging them together, using specified methods, such as fields and the nature of the merge. Depending on data relationships, the resulting merge can produce a one-to-one or one-to-many output.</li>
    <br>
    <li><b><code>on='col'</code></b> - Specifies the field(s) the merge will be performed on, e.g. an <code>id</code> field merge requires an <code>id</code>column present in both data frames. Alternatively, if the column names differ between data frames, <code>left_on</code> and <code>right_on</code> are specified.</li>
    <br>
    <li><b><code>how='inner/left/right/outer'</code></b> - Describes the nature of the join, with each producing different results. These are explored below.</li>
</ul>

<br>
