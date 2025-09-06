// QuoteContract.ts
import { Contract, GlobalState } from "some-smart-contract-framework"; // Replace with actual framework, e.g., beaker, algob, etc.

export class QuoteContract extends Contract {
  quoteOfTheDay = GlobalState<string>({
    key: "quote",
    initialValue: "No quote yet.",
  });

  setQuote(quote: string): string {
    this.quoteOfTheDay.value = quote;
    return quote;
  }

  getQuote(): string {
    return this.quoteOfTheDay.value;
  }
}

