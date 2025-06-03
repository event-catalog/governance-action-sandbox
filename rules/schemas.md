## Event Design Guidelines

1. **Schema Changes Must Be Backward Compatible**  
   Any updates to event schemas must not break existing consumers. Always maintain backward compatibility.

2. **Design Events to Be Idempotent**  
   Events should be safe to process multiple times without causing unintended side effects.

3. **Use Domain-Specific Event Types**  
   Avoid generic events like `EntityUpdated`. Instead, use clear and specific names that reflect the domain and action, such as `OrderShipped` or `InvoiceGenerated`.

4. **Include a Version Number in All Events**  
   Every event must include a version number to enable clear evolution of the schema over time.

5. **Assess Impact on Downstream Consumers**  
   Before making any changes, evaluate how updates will affect existing consumers and ensure they can safely handle the change.
