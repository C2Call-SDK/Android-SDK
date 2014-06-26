Android-SDK
===========

C2Call Social Communication Android SDK V 0.8.24 (Beta) Release Notes
===========

Major fixes/changes:
    - Implemented method to transfer master credit to users:
        SCCoreFacade.addCredit(int valueInCent, SCCurrency currency, String transactionId, String receipt)
        Example:
            SCCoreFacade.instance().addCredit(10, SCCurrency.Euro, UUID.randomUUID().toString(), null);
            
    - Removed third-party dependency to jackson-core-asl-1.9.1.jar, that caused a conflict when working with Google+ libraries
    
    - Fixed some issues related to swallowed events when the current Activity is not a subclass of SCBaseFragmentActivity.
        This could cause an empty friend list or call history
