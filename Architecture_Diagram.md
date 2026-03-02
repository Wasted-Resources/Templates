classDiagram
    class DummyClass {
        -Profile _Profile
        -Data _data
        +SaveData()
        +LoadSlotData(int index)
        -InitializeSave(int index)
    }
    class Profile {
        +string UserName
        +string UserId
        +List~Data~ Datas
    }
    class Data {
        +int SessionId
        +int SlotIndex
        +Statistics statistics
    }
    class RestApi {
        <<static>>
        +AddSession()
        +UpdateSession()
    }

    DummyClass "1" --> "1" Profile : manages
    Profile "1" *-- "many" Data : contains
    DummyClass ..> RestApi : synchronizes via