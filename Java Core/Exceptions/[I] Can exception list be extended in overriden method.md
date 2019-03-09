## Can exception list be extended in overridden method?
No, because in this case it doesn't follow the contract of its superclass. The client doesn't expect the Exception from your children so list can't be changed.
