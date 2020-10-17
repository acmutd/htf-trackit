# PEG Ratio Resources

For more information about the PEG ratio of a stock: [https://www.schwab.com/resource-center/insights/stock-analysis-using-the-peg-ratio](https://www.schwab.com/resource-center/insights/stock-analysis-using-the-peg-ratio)

# EPS Ratio Resources

For more information on the EPS of a stock: [https://www.investopedia.com/terms/e/eps.asp](https://www.investopedia.com/terms/e/eps.asp)

# Annotated `save_graph()` Method

```python
# save_graph method
"""
save_graph()
- Generates an infographic.
"""
def save_graph(ticker, price_history, logo_url, short_name, industry, discord_tag, overvalued, peg_ratio):
	# generates the words 'overvalued' or 'undervalued'
    ov_txt = 'overvalued' if overvalued else 'undervalued'
    # avoid axis overlap
    fig = plt.figure(figsize=(10,12), dpi=300, constrained_layout=True)
    # Use GridSpec for customising layout
    # This makes a 6x4 grid for laying out our infographic
    gs = fig.add_gridspec(nrows=6, ncols=4)
    # Logo image
    logo_image = fig.add_subplot(gs[0, 0])
    logo_image.axis('off')
    # This will download our image into `logo.png`
    urllib.request.urlretrieve(logo_url, 'logo.png')
    stock_image = plt.imread('logo.png')
    # This will put the image on our infographic
    logo_image.imshow(stock_image)
    # Text
    text = fig.add_subplot(gs[0, 1:])
    text.axis('off')
    # This will put text on our infographic
    text.text(0, 0.7, short_name, horizontalalignment='left', verticalalignment='center', fontsize=30, fontweight='bold')
    text.text(0, 0.4, f'Ticker: {ticker}', horizontalalignment='left', verticalalignment='center', fontsize=20)
    text.text(0, 0.0, f'{industry}', horizontalalignment='left', verticalalignment='bottom', fontsize=20, fontstyle='italic')
    # Overvalued?
    ov = fig.add_subplot(gs[1, :])
    ov.axis('off')
    # This will put your discord tag and the overvalued evaluation on here
    ov.text(0.5, 0.85, f'{discord_tag}', horizontalalignment='center', verticalalignment='center', fontsize=30, fontweight='bold')
    ov.text(0.5, 0.65, f'determined this stock was', horizontalalignment='center', verticalalignment='top', fontsize=20)
    ov.text(0.5, 0.00, f'{ov_txt}', horizontalalignment='center', verticalalignment='bottom', fontsize=40, fontweight='bold', color='darkred')
    # Graph
    stock_graph = fig.add_subplot(gs[2:5, :])
    stock_graph.set_title('YTD Stock Price')
    stock_graph.plot(price_history.index, price_history['Close'], linewidth=3)
    # Display PEG ratio
    peg = fig.add_subplot(gs[5, :])
    peg.axis('off')
    peg.text(0.5, 0.5, f'PEG Ratio: {peg_ratio}', horizontalalignment='center', verticalalignment='center', fontsize=30, fontstyle='italic', fontweight='bold')
    plt.savefig(f'{ticker}.png', facecolor='white', transparent=True, bbox_inches='tight')
```