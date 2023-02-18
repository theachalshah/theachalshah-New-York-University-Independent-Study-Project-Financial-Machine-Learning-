# theachalshah-New-York-University-Independent-Study-Project-Financial-Machine-Learning

Steps Summary:-

n securities with highest daily volatility are chosen.

Fractional Differentiation is used instead of integer differentiation(These have a memory cut-off, in the sense that history is disregarded entirely after a finite sample window.) Fractional Differentiation preserves memory and also attains stationarity. At d = 0.35 the correlation is still very high, at 0.995.

Combinational Purged Cross-Validation Method – Given a number 𝜑 of back test paths targeted by the researcher, CPCV generates the precise number of combinations of training/testing sets needed to generate those paths, while purging training observations that contain leaked information. This one alternative approach is to use some combinatorial tricks to generate multiple back test paths. For those cases where purging is not able to prevent all leakage, we can impose an embargo on training observations after every test set. This method avoids serial correlation.

MLP(Multi Layered Perceptron) model is used to train/test and validate out of sample data next day of Fractionally Differentiated Series. Root Mean Squared Error is calculated for train and test set.

For both real(market data) and predicted(model predicted out of sample outcome) signals are marked as 1(Long) and -1(Short) for percentage daily change of more than 2% in fractionally differentiated series on positive and negative sides respectively. Assumed 2% minimum to cover transaction fees, broker fees and slippage. These signals are used to calculate gain/loss on original series. real_profit_loss and predicted_profit_loss are calculated by buying/selling on Open and selling/buying on Close for more than 2% in fractionally differentiated series on positive and negative sides.( Note: profit_loss is only for one quantity traded over. If z quantity is traded then profit_loss will be z*profit_loss)
