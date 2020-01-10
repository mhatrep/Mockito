# Test Doubles
1. Dummy
2. Fake
3. Stub
4. Mock

# Mockito 

Mocking in Mockito is performed using when(obj).then*() in the Arrange step.
Later, interaction with our mock can be validated using verify() in the Assert step.

## Enable Mockito - 3 Ways
1. @RunWith(MockitoJUnitRunner.class)
2. MockitoAnnotations.initMocks()
3. MockitoJUnit.rule()

## Mock Methods

1. Simple Mocking
MyList listMock = mock(MyList.class);
when(listMock.add(anyString())).thenReturn(false);
2. Mocking with Mock's Name
3. Mocking with Answer (implements Answer<Boolean> )
4. Mocking with MockSettings


## ArgumentMatchers


----------------------------------------------------


@Mock - create and inject mocked instances without having to call Mockito.mock manually
@Spy - spy on an existing instance.
@Captor - create an ArgumentCaptor instance
@InjectMocks - inject mock fields into the tested object automatically.


----------------------------------------------------

Mockito.when(wordMap.get("aWord")).thenReturn("aMeaning");



----------------------------------------------------

Mockito's annotations minimize repetitive mock creation code
They make tests more readable
@InjectMocks is necessary for injecting both @Spy and @Mock instances




## BDDMockito
import static org.mockito.BDDMockito.*;

write our Arrange step using given (instead of when), likewise, we could write our Assert step using then (instead of verify).

