# Retirement Savings Calculator

How much can you spend each month in retirement, and will your savings last? Enter what you have saved today, a monthly amount you will add until you retire, and how many years the money has to last. The calculator shows the monthly spending that covers those years and whether anything is left over.

**Live:** https://retirement-calculator-190.pages.dev

## What it models

Everything runs in monthly steps.

1. **Building your savings.** Each month until retirement you add your contribution, and the balance grows at your projected pre-retirement return. You can raise contributions with inflation.
2. **Retirement.** Each month you withdraw enough to cover that month's spending. You enter spending in today's dollars. The calculator inflates it to the year you retire, uses that larger figure as your first withdrawal, and keeps raising it with inflation so it holds its purchasing power. Savings grow at your (usually lower) in-retirement return.
3. **Taxes.** Pick an account type:
   - **Traditional 401(k) / IRA:** the whole withdrawal is taxed at your income tax rate.
   - **Roth 401(k) / IRA:** withdrawals are tax free.
   - **Taxable brokerage:** tax applies only to the gain above your average cost basis, which blends what you hold today with what you add along the way.

### Inputs

| Input | Meaning |
| --- | --- |
| Account type | Traditional, Roth or taxable. Decides how withdrawals are taxed |
| Saved today | The balance you start with |
| Add each month | Dollars contributed each month until you retire |
| Years until retirement | How long you keep contributing |
| Raise contributions with inflation | Optional. Grows the contribution by the inflation rate |
| Years the money must last | Length of retirement |
| Spending to test per month | In today's dollars. Leave at 0 to test the maximum |
| Return before / in retirement | Projected annual returns for each phase |
| Inflation per year | Applied to spending (and to contributions, if the option is on) |
| Tax rate | Income tax rate (traditional) or capital gains rate (taxable). Hidden for Roth |
| Cost basis | Average amount you paid in for what you hold today. Taxable accounts only |

### Outputs

- The monthly spending, in today's dollars, that uses all your savings over your chosen years
- Savings at retirement, in future and today's dollars
- Total contributed over the years you save
- The most you could spend per month forever, when that is possible
- For a spending level you choose: what it equals in retirement-year dollars, whether it lasts, and how much is left or when it runs out
- A chart of your savings over time, in today's dollars

### The "forever" figure

Spending forever only works if your in-retirement return outpaces inflation by enough to cover tax. When it does not, the page says so instead of showing a number. Setting a finite number of years always works.

## What it does not model

It assumes returns are constant. Real markets swing, so a projection can be right about the average and still wrong about the path. There is no volatility or sequence-of-returns risk, no progressive tax brackets, no early-withdrawal penalties, no required minimum distributions, no Social Security or pension income, and no investment fees. Treat the results as scenarios, not forecasts. This is arithmetic, not financial advice.

## Run it locally

There is nothing to install or build. Open `index.html` in a browser. The page makes no network requests except loading a web font, and no data leaves your device.

## Publish with GitHub Pages

1. Push `index.html`, `README.md` and `LICENSE` to a GitHub repository.
2. In the repository, go to **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, select `main` and the `/ (root)` folder, then save.
4. After a minute or two the site is live at `https://<your-username>.github.io/<repository-name>/`.

## Credits

Adapted from the [Bitcoin Retirement Savings Calculator for Plebs](https://github.com/chriso22/Bitcoin-Retirement-Calculator-for-Plebs), which uses the same savings-then-withdrawal approach for a bitcoin stack.

## License

Released under the [MIT License](LICENSE).
