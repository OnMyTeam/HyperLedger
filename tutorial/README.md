# hyperledger fabric



## Transaction flow
�Ʒ��� �����۷��� �к긯���� Ʈ����� ó�� ������ �����մϴ�.<br>
�����۷��� �к긯�� ó�� ���ϴ� ������� ���� �ִ��� ���� �����Ϸ��� ����� �߽��ϴٸ�...<br>
�ƹ����� �� �־ �ͼ����� ���� ������� �ټ� ����� ���� ������ ū �帧�� �־ Ʈ������� ��� ó���Ǵ����� �����ص� ������ ���� �ǽ� �Ŷ� �����˴ϴ�. �Ʒ��� ������ [�к긯 ����](https://hyperledger-fabric.readthedocs.io/en/v2.2.0/txflow.html?highlight=transaction%20flow)�� `transaction flow`�κ��� �������� ������ ���̴� �ڼ��� ������ ���Ͻô� ���� ���� ������ �����Ͻñ� �ٶ��ϴ�.
<br><br>
### 1. Assumptions
<br>
Ʈ����� ó�� ������ �����ϱ� �� �̹� ä���� �����Ǿ��ְ� ��Ʈ��ũ�� ���� ���̸�, Ʈ������� �����ϴ� ����ڴ� CA(Certificate Authority)�� ���� register�� enroll�� �Ǿ��־� ��Ʈ��ũ�� �����ϴµ� �ʿ��� ����(Certificate)�� �߱޹޾Ҵٰ� �����մϴ�.<br>
chaincode�� �� Peer�� ��ġ �Ǿ��ְ�, ��ġ�� ü���ڵ忡�� Ʈ����ǿ� ���� ����� �Լ����� ���ǵǾ��ֽ��ϴ�. chaincode�� ��ġ�� Peer�� Ʈ������� ������ �ݵ�� ����(simulation)�� �ؾ��ϰ� �� ����� Client���� ������ �־�� �մϴ�.

<br><br>
### 2. Client A initiates a transaction
<br>
<img src="images/image1.jpg" alt="drawing" width="700"/><br>
Client�� application(���� ����Ʈ)���� Ư�� ������ �����ϴ� ��ư�� �����ٰ� �����մϴ�. ��ư�� ������ �Ǹ� SDK�� ���� Ư�� ������ �����ϴ� ������ ����ϴ� �Լ��� chaincode���� �����϶�� transaction proposal�� Peer���� ������ �˴ϴ�. transaction proposal���� 





